# test-run
A Python library for tests with meaningful output and display (IDLE-compatible)

This testing module is intended for small-scale testing of python, including
    in IDLE. Notable features include:

`TestRun`: 
  A base class for a test-suite, including automatic test-detection 
  (for methods beginning with 'test_'), running all available tests or a 
  specified set with 'run_tests', running the tests which failed in the last 
  run with 'run_failed_tests', and automatic (not in IDLE) and user-generated 
  timeouts while testing.

`TestGroup`: 
  A class for grouping multiple TestRun instances as though they are a single 
  instance.

`Redirect`: 
  A class for stream redirection and multiplication, focused on stdin, stdout, 
  and stderr, but also usable for general file streams. Allows for capturing 
  printed output and simulating typed input while testing.

`MultiRedirect`: 
  A class for managing multiple redirections, allowing for methods to be run 
  simultaneously run on all stored redirections.