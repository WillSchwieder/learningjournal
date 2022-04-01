---
layout: post
title: Three things I learned from The Ruby Koans
---
Some believe that the path of enlightment can only be saught through introspection but turns out all we needed was a computer program. To get further into the nuts and bolts of true Ruby programming, we are going to be looking at the Ruby Koan module created by Jim Weirich at EdgeCase. More than just getting the console to spit out what I was looking for, I struggled to figure out what exactly the change I needed to implement to move on to the next section. My approach was therefore to attempt to minimize the changes I was making and only operate within the __ provided, or at least as much as possible.  


Here are a couple of things I learned from [The Ruby Koans](http://rubykoans.com/):
1. The += can be used to quickly concantenate strings in Ruby (I always end up with problems that can be solved some quickly concatenation)
2. The shovel operator (<<) will not only affect the specified variable but the variable that was used to originally set that variable (if there is one)
3. The * (or "splat") operator will assign multiple values to a single dictionary entry (so last name can be [Smith, III])
4. Default values within arrays and hashes can be powerful
5. Fetches and KeyErrors may be helpful when handling hashes to ensure that values are checked and handled correctly (rather than just relying on hash and nils)
6. Arrays have numerous methods for inserting values at the beginning or the end (pop or shift). Could be helpful for linked lists or other similar applications
7. Regular expressions are stil incredibly difficult in Ruby but a couple of shortcuts include (cause I know I'll never remember them):
    - [/[0-9]+/]
    - OBJECT.select { |a| a[/[cbr]at/] }
    - [/\d+/]
    - [/[a-zA-Z0-9_]+/]
    - Honestly, there are too many to paste all of them here so just refer back to the "about_regular_expressions" module when you're Googling this in the future.
8. There is an "unless" option within if statements that acts as a falsifier
9. Why does the following code work?
    - def test_break_statement
        i = 1
        result = 1
        while true
        break unless i <= 10
        result = result * i
        i += 1
        end
        assert_equal 3628800, result
10. Proper way to handle a particular error:
    - def test_raising_a_particular_error
            result = nil
            begin
      raise MySpecialError, "My Message"
    rescue MySpecialError => ex
      result = :exception_handled
    end    

11. I have no clue what inject does with Arrays, will need to do more reading
12. The last piece of the blocks is fuzzy to me as well. 
13. Classes operate very similarly to Python classes, class define then method define, self classes intialize objects within a class
14. To initialize an attribute in a class use "attr_reader :values" where "values" is replaced by whatever attribute you want to initialize. Very similar to Python.
15. Actually this is even closer to what I am used to in Python: 
    - def self.class_method2
      :another_way_to_write_class_methods
    end



--- 



