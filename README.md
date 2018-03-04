# system_utils
This is a simple library for dealing with "system" related things in MATLAB. Includes a class-based approach to dealing with directories and files.

# Installation instructions:
```
git clone https://github.com/justinblaber/system_utils.git
```
Then, in MATLAB:
```
>> addpath('system_utils');
```
You can try out some of the utilties like so:
```
% Make a test directory
test_dir = system_utils.directory('test');
test_dir.mkdir();

% Create a test file
test_file = system_utils.file(test_dir,'test.txt');
test_file.dlmwrite([1 2 3]);

% Copy test file
test_copy_file = test_file.cp(test_dir,'test_copy.txt');

% Read contents of test file
test_copy_file.dlmread()

ans =

     1     2     3
```
