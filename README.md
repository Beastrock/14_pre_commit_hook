# Basic description 
**Pre-commit hook** - file which launches when user tries doing the commit for preventing wrong changes to be done in repository. If pre-commit file ends with any type of error, the commit won't be done. Saying more concrete this situations are reached if pre-commit file doesn't ends with end process code 0. 

We can use Python programming language, Ruby and Perl.   
  
For using pre-commit file you need to put it in `.git\hooks` and named it `pre-commit` without any extension or you can rename existing `pre-commit.sample` which is already in that directory. 
  
# Pre-commit creating example
In this task of the devman we have to test `quadratic_eqution.py` by unittest file `test.py` before committing. 
So let us simply create pre-commit for this:   
1) create a file `pre-commit` with such content:  
  `#!/bin/sh`  
  `python tests.py`  
2) Move it to the hooks folder.  
  
# Futher learning sources
+ A framework for managing and maintaining multi-language pre-commit hooks: [pre-commit by Yelp](http://pre-commit.com). 
+ Chapter from GIT book about pre-commit and other availible hooks: [Настройка Git - Перехватчики в Git](https://git-scm.com/book/ru/v1/%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0-Git-%D0%9F%D0%B5%D1%80%D0%B5%D1%85%D0%B2%D0%B0%D1%82%D1%87%D0%B8%D0%BA%D0%B8-%D0%B2-Git).

