# Ruby Loops


```ruby
# IF-ELSE
num = 0
if num<0
  puts "negative number"
elsif num>0
  puts "positive number"
else 
  puts "number equals 0"
end

# short IF
puts "Its true" if true

# ternary If ELSE -> NOT DOING ANYTHING, returning a result!!
condition = false
condition ? return_if_true : return_if_false
```

```ruby
# SWITCH
case language
  when "JS"
    puts "Websites!"
  when "Python"
    puts "Science!"
  when "Ruby"
    puts "Web apps!"
  else
    puts "I don't know!"
end

# fast switch
case language
  when "JS" then puts "web"
  when "html" then puts "web"
  when "ruby" then puts "rails"
  else puts "Error!"
end
```

```ruby
# UNLESS (opposite of "IF")
problem = false
unless problem	# if not
  puts "we have a problem"
else 
  puts "no problemo amigo!"
end
# unless shortcut (when no "else" is needed)
puts "we have no problem" unless problem	# short notation (same code)

# UNLESS ONE LINER
puts "not true" unless true
```

```ruby
# WHILE
i = 0
while i<5
  puts i
  i += 1
end
```

```ruby
# UNTIL (opposite of "while")
i += 1
until i == 6
  puts i
  i += 1
end
```

```ruby
# FOR-Loop
# include last number
for num in 1..10		# 2 dots!
  puts num
end
# exclude last number
for num in 1...10		# 3 dots!
  puts num
end
# with steps
for num in (1..100).sep(10)   # 10er schritte 
  puts num
end

# NEXT
for i in 1..5
  next if i % 2 == 0
  print i
end
```

```ruby
# DO WHILE
i = 1
loop do 
  puts i
  i += 1
  break if i > 5
end
# DO SHORTCUT
i = 1
loop {  			# "{" replaces "do"
  puts i
  i += 1
  break if i > 5
}					# "}" replaces "end"
```

```ruby
# FOR EACH ELEMENT OF OBJECT
array = [1,2,3,4,5]		# defining array
#version 1
array.each do |x|
  puts x	
end
# alternative version (same code)
array.each { |x| puts x }
array.sort 					# sorts array ins ASC order (works for strings and numbers)

# TIMES ITERATOR
n = 10
n.times { print "hello\n"}
```

```ruby
# UPTO / DOWNTO BLOCKS
95.upto(100) {|x| p x}
15.downto(0) {|x| p x}
"A".upto("X") {|x| puts x}
```

```ruby
# COLLECT /same as MAP
# manipulates each element of an object and returns the full object
array = [1,2,3,4]
puts array.collect {|x| x+1} 	# returns manipulated object (new one)
array.collect! {|x| x+1}		# object manipulation (add +1 to each item in the same array)
array.map! {|x| x+1}	# map does the same than collect!

# SELECT
# selects each element of object given condition
# .select! VS .select
```


```ruby
# METHODS
# methods must be defined before calling them! ruby doesnt "search" for methods 
# define method
def title(msg, n, del)
  puts " #{msg} ".center(n, "#{del}")
end
title("title1", 20, "-") 	# call the method

# SPLAT arguments (not neccessary but possible)
def greeter(string, *friends) 
  friends.each {|friend| puts "#{string}, #{friend}"}
end

# default parameters
def my_reverse(val1, val2=false) 
  val1.reverse!
  if val2 
  	puts "msg to console enabled!"
  end
  # val2s default value is true
end

# IMPLICIT RETURN
# -> last executed action is returned
def add(a,b)
  a + b
end
```

```ruby
# BLOCKS (nameless methods)
10.times do
  puts "hello!"
end
10.times {puts "hello!"}

# YIELDING
def yield_name(name)
  puts "In the method! Let's yield."
  yield("Kim")
  puts "In between the yields!"
  yield(name)
  puts "Block complete! Back in the method."
end
yield_name("Eric") { |x| puts "My name is #{x}." }
```

```ruby
# PROCS -> blocks as methods!
cube = Proc.new { |x| x ** 3 }
# converting procs into blocks with "&"
&cube # -> proc converted to Block
```

```ruby
# LAMBDAS #similar to procs
# Like procs, lambdas are objects. The similarities don't stop there: with the exception
# of a bit of syntax and a few behavioral quirks, lambdas are identical to procs.
# syntax: lambda { |param| block }
lambda_name = lambda { puts "Im inside the lambda!"}
&lambda_name # converts lambda to a block

# LAMBDA VS PROC
# - when inside a method, Proc returns immediately, lambda returns to the calling method
# - lambda checks number of arguments! It will throw an error if it doesnt match. Procs dont do that
```



```ruby
# CLASSES
# nameConvetion: CamelCase  and Capitalized
class Person		# class definition
  @@person_count = 0
  initialize(name)		# constructor
  	@name = name 		# @name is an instance variable (non-static fields in java)
  	@@person_count += 1	
  end
  # self. can be replaced by the Classname!
  def self.number_of_instances		# instance methods! NON STATIC METHODS. Class-Methods in Java
    return @@person_count
  end
end

# VARIABLES/METHOD VISIBILITY & CONCEPTS
$variable	# global variables = making variables visible outside of its method
@variable	# instance variables
@@variable	# class variables: all instances of a class have access to THE SAME variable!

# INHERITANCE
# < is read as "inherits from" or "is a"
class Item
  def say_smth
  	return "im an item"
  end
end
class CD < item 	# CD inherits from item (is-a relationship)
  def say_smth		# when same class method names: overrides method of the "upper" class
	return "im a cd"  	
  end
end

# When you call super from inside a method, that tells Ruby to look in the superclass 
# of the current class and find a method with the same name as the one from which super 
# is called. If it finds it, Ruby will use the superclass' version of the method.

# ONLY ONE INHERITANCE IN RUBY
# Not allowing multiple inheritance

# object.method (object is the "RECIEVER" of the method "method")

# Setter & Getter
class Person
  attr_reader :name
  attr_accessor :job
  attr_writer :password
  def initialize(name, job, password)
    @name = name
    @job = job
    @password = password
  end
  
  def name
    @name
  end
  
  def job=(new_job)		# ruby convention of setters: "name_of_method=" -> the equals sign belongs to the name
    @job = new_job
  end
end

attr_writer :name   # setter function short. eg: Person.name="Mark"
attr_reader :name   # getter function short. eg: Person.name
attr_accessor :name # setter + getter function initizalized!
```

```ruby
# MODULES
# similar to objects, but you cant initialize instances of them, the just STORE things
module Circle
  CONSTNAT_PI_ALL_CAPS = 3.14 # constants can be changed, but shouldnt! Ruby warns you if you want to do it
end
# accessing constant from outside the module (with two ":")
Circle::CONSTNAT_PI_ALL_CAPS 

# importing modules
require 'circle'  # import modules, always small_cases. You can acces the methods with Circle.method()
include Circle    # only in class sphere, to import a module into a class!
                  # imports so we dont need to use the ModuleName::GLOBAL_VAR notation and can just write GLOBAL_VAR


# INCLUDING VS EXTENDING!
module ThePresent
  def now; puts Time.now; end
end

class TheHereAnd
  extend ThePresent 
  include ThePresent 
end

TheHereAnd.now          # access module method through extended (Class as whole acceses module method)
TheHereAnd.new().now    # access module method through inclusion (instance of an object accesses method)
```
