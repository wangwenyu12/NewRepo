# NewRepo
infChar.tvRatio = 0.69;
infChar.VSS = infChar.TSS.*infChar.tvRatio; % mg/L, volatile SS
infChar.FSS = infChar.TSS - infChar.VSS; % mg/L, fixed SS
infChar.cBOD = InfluentData(:,3); % mg/L
infChar.TKN = InfluentData(:,4); % mg-N/L
infChar.NH3 = InfluentData(:,5); % mg-N/L
infChar.NO3 = InfluentData(:,6); % mg-N/L
infChar.BOD = infChar.cBOD; % mg/L
infChar.ALK = InfluentData(:,7); % mg/L
% Conversion to ASM1 variables using Bi