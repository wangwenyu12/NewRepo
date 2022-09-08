# NewRepo
infChar.tvRatio = 0.69;
infChar.VSS = infChar.TSS.*infChar.tvRatio; % mg/L, volatile SS
infChar.FSS = infChar.TSS - infChar.VSS; % mg/L, fixed SS
infChar.NH3 = InfluentData(:,5); % mg-N/L
infChar.NO3 = InfluentData(:,6); % mg-N/L
infChar.BOD = infChar.cBOD; % mg/L
infChar.ALK = InfluentData(:,7); % mg/L
% Conversion to ASM1 variables using Bi
% Grady, Daigger, Love and Filipe, from Chapter 9.6, for CODt and CODbo
% constant values
infChar.CODt = 2.1.*infChar.BOD; % mgCOD/L, Converts BOD5 to total COD, if not available
infChar.CODbo = 1.71.*infChar.BOD; % mgCOD/L, biodegradable COD
infChar.CODio = infChar.CODt - infChar.CODbo; % mgCOD/L, inert COD