# 14_pre_commit_hook (Quadratic Equation Solving Script)  

This script solves quadratic equations with non-complex roots.  
 
## Getting Started  

Clone repository:   
`$ git clone https://github.com/Beastrock/14_pre_commit_hook.git`    

## Usage
###Adding to projects
To add solving function import:  
`from quadratic_equations.py import get_roots`   

###Basic usage
 
`root1,root2 = get_roots(a, b, c)`,  
where a, b, c is coefficients of quadratic equation you need to solve.
  
## Tests  

The `get_roots` function is tested to prevent getting wrong roots and other errors by checking on correctness returning roots from different area values. It is performed by using <i>pre-commit hook</i> file which launch unittests file `tests.py`.  

**Pre-commit hook** - file for preventing wrong changes to be done in repository. It launches when user tries to commit. If pre-commit file ends with any type of error, the commit will not be done. Saying more concrete, these situations are reached if pre-commit file does not over with end process code 0. 

To install tests put `pre-commit` file to `.git\hooks`.

### Running tests example
+ Updating solving function with making a mistake and trying to commit will lead to test's error:
  
`$ git commit -m "Update solving function"`  
`ERROR: test_first_root_less_than_second (__main__.QuadraticEquationTestCase)`    
  
`Traceback (most recent call last):`  
  `File "tests.py", line 12, in test_first_root_less_than_second`  
    `root1, root2 = get_roots(1, 2, -3)`  
`TypeError: 'NoneType' object is not iterable`  
  
  
`Ran 4 tests in 0.001s`
  
`FAILED (errors=1)`  
  
Now all files are in status "modified" again. It can be checked by `$ git status` command. 

+ Updating solving function correctly will lead to successful test run and committing changes:  
    
`$ git commit -m "Update solving function"`  
`Ran 4 tests in 0.000s` 

`OK`  

