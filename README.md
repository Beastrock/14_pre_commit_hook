# 14_pre_commit_hook  
This script illustrates a simple example of using pre-commit hook with Python unittests. The tested scrypt is `quadratic_equation.py` which solves quadratic equations with non complex roots. `Tests.py` test the `get_roots` function to prevent getting wrong roots and other errors. It is done by checking on correctness returning roots from different area values.

# Basic description 
**Pre-commit hook** - file which launches when user tries doing the commit for preventing wrong changes to be done in repository. If pre-commit file ends with any type of error, the commit won't be done. Saying more concrete this situations are reached if pre-commit file doesn't ends with end process code 0. 

We can use Python programming language, Ruby, Perl and some others .     
 
# Pre-commit setup  
For using pre-commit file you need to put it in `.git\hooks` and named it `pre-commit` without any extension or also you can rename existing `pre-commit.sample` which is already in that directory.  

Let us setup the example code pre-commit:  

1) Clone the script by following commands:  
  `git clone <repository url>`  
  
2) Move  `pre-commit` file to `.git\hooks`  

3) Change `quadratic_equation.py` by deleting '# useless comment` on the last line of script  

4) Commit changes  
If all is alright you will see this in the console:  
`$ git commit -m "Add explanation of using the script"  
....
----------------------------------------------------------------------  
Ran 4 tests in 0.000s  

OK`  
    
4) No to see how pre-commit prevent commiting replace returning on 11 and 12 lines  

5) Try to commit changes  
You will see this:  

No you have all files in status modified again. No chance for bad programmists' commits!  
6) Profit! Now you know how pre-commit hook works  
  
# Futher learning sources
+ Chapter from GIT book about pre-commit and other availible hooks: [Настройка Git - Перехватчики в Git](https://git-scm.com/book/ru/v1/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-Git-%D0%9F%D0%B5%D1%80%D0%B5%D1%85%D0%B2%D0%B0%D1%82%D1%87%D0%B8%D0%BA%D0%B8-%D0%B2-Git).  
+ A framework for managing and maintaining multi-language pre-commit hooks: [pre-commit by Yelp](http://pre-commit.com).

