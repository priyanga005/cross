% Cross-correlation in MATLAB
clc;
clear;

% Input signals
x = [1, 2, 3];    % First signal
y = [0, 1, 0.5];  % Second signal

% Compute cross-correlation
r = xcorr(x, y);

% Display results
disp('First Signal (x):');
disp(x);
disp('Second Signal (y):');
disp(y);
disp('Cross-correlation Result (r):');
disp(r);

% Plot the result
lags = -(length(y)-1):(length(x)-1);  % Lag values
stem(lags, r, 'filled');
xlabel('Lag');
ylabel('Cross-correlation');
title('Cross-correlation of the Signals');
grid on;
