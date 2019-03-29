# Ruby Notes

```ruby
#RUBY PROJECTS AS EXCERCISE
# - game of life with GUI
# - calculator
# - sudoku solver (backpropagation)
# - file input reader -> word analyzer / char analyser

# TAKE HOME
# CRUD for create, read, update, and delete

# TAKE HOME 2
# Normally type checking is not done in Ruby, but instead objects are assessed
# based on their ability to respond to particular methods, commonly called “Duck
# typing”. In other words, if it responds to the methods you want, there’s no
# reason to be particular about the type. 

# TAKE HOME 3
# almost everything is an object in ruby! Only exception are blocks!
```

```ruby
# DATA TYPES IN RUBY
- symbols # Symbols are unique identifiers that are considered code, not data
- numbers # integer VS floats

# while strings represent data that can change, symbols represent unique values, which are static.
# if the text at hand is "data", then use a string. If its code, then use a symbol, especially when used as keys in hashes

# TESTING IN SANDBOX
# ruby irb: TESTENVIRONMENT IN CMD
irb   # start IRB = Interactive Ruby (Shell)
irb 

# DETERMINE DATA TYPE IN RUBY (anyways)
p 1.instance_of? Integer   #=> True
p "1".instance_of? String  #=> True
p [1,2].instance_of? Array #=> True
# alternative: is_a? (type)
p 1.is_a? (Integer)       
p "string".is_a? (String) 

# DISPLAY TO CONSOLE
puts "hello, World!"	# adds newline at end
print "hello, World!"	# no newline at end
print "hello,", 250, " World"   # print different types (separate by comma)

# STRING OPERATIONS
.chomp			# cuts last separotr? not sure yet.
.upcase					# 
.downcase				# Uppercase converted to downcase
.capitalize				# First character capitalized, others converted to downcase
.reverse				# returns reversed string
.length					# returns length of string
"hello,World".split(",")	# splits string by delimitter, outputs array
.strip() 				# eliminates leading and ending whitespaces
.index()
.center(6, '-')	
"Aksc" < "B"  # true! compares first letter! Capitalization is important though!

# general substitution! replaces all instances of "f" with "F"
.gsub(/f/, "F")		
.nil?				#check if value is nil	

# title methods
"hi".center(6, '-')		# // --hi--
" hi ".center(12, '-')	# // ---- hi ----

# OBJECT MODIFIERS (shortcut)
name.upcase!	# same as name = name.upcase
name.gsub!(/f/, "F")

# QUESTIONMARK FUNCTIONS
# general rule: functions ending with "?" evaluate to true/false
.include? "substring"	# matches substring -> returns true/false
"name".eql? "name"		# true
"name".eql? "nam"		# false
"name".include? "m"		# true
"name".include? "x"		# false
"name".index("a")		# 1
"name".index("me")		# 2

# EQL? method can be used on all objects?
1.eql? 1
x = [1,2,3]
x.eql? [1,2,3]

# MTHODS FOR INTEGERS
12.next   # // 13 (doesnt work for floats)


"Thomas Starzynski"[0,3] 			# Tho
"Thomas Starzynski".index("Star") 	# 7
"Thomas Starzynski"[7,1] 			# Starzynski

# STRING INTERPOLATION vs CONCATENATION
puts "my name is #{name}"	  # interpolation
puts "my name is "+name     # concatenation
puts "my name is " << name  # concatenation with shovel (concatenation operator)


# relational operations
==	 	# equal
!=		# not equal
<		# less than
<=		# less than or equal
>		# greater than
>=		# greater than or equal

# logical / boolean operators
&&		# and (short circuit)
||		# or (short circuit)
!		# not

# why does short circuit matter?
# -> when having || the order is important
# -> it can happen that you can avoid throwing an exception by correct order

# assignment shortcuts
num += 1	# num = num + 1
num -= 1	# num = num - 1

# shovel parameter <<
# to push something (push = add at the end)
# e.g. push a new value to an array
x = [1,2,3]
x.push(4,5,6)
x << 7    # push multiple values is not possible with shovel right?

x = [1,2,3]
x.push(4,5,6)     # pushing multiple objects is easy with "push"
x << 7 << 8 << 9  # pushing one object is better with shovel
```

```ruby
# conditional assignments!
||=   # only assign value if there is no value assigned yet! (first checks the variable)
name = "asd" unless name.nil?   # alternative to think about this operator
# EXAMPLE CODE
name = nil
name ||= "thomas"   # name has not assigned a value yet (nil=no assignment), so it gets assigned
name ||= "sam"      # since name is already assigned, nothing happens here

# Multiple operations on one line
print "Hello, "; puts "world!"; puts " three";
p "Hello"
p [1,2,3,4].to_s

# ARRAYS
array = [1,2,3,4,5]		# create array with 5 numbers
array[0]				# acces first element
array.push(12)			# adds value to array at the end!

string_array = ["hello"," ","world","!"]

# MATRICES
matrix = [[1,2,3],[4,5,6],[7,8,9]]
matrix.each {|row| row.each {|x| puts x}}	# iterate over all elements

# HASHES
my_hash = { 		# HASH ROCKET STYLE =>
  key1 => value1,	# seperated with comma!!!
  key2 => value2,	# seperated with comma!!!
  key3 => value3	# no comma!!!
}
# creating hashes
my_hash = Hash.new(default_value)	# without default value: Hash.new
my_hash[key1] = value1
my_hash[key2] = value2
my_hash[key3] = value3
# new syntax since ruby 1.9!!! (similar to javascript!)
movies = {
  start_wars: "amazing film!",
  titanic: "but this ship can't sink!!",
  troja: "Heeeeectoooooorrrr!",
}
# call hash
my_hash[key1]	# like an array
# iterate over hash
hash.each do |key,value| 
  print "key: #{key}, value: #{value}"
end
# hash default value
my_hash.each_key   		# iterate over all keys
my_hash.each_value		# iterate over all values
```



```ruby
# UNKLAR:
freq = {
  "thomas" => 1,
  "mark" => 323,
  "alex" => 15
}
freq = freq.sort_by do |key, val|
  val
end
freq.reverse!
# sorting by key or value
freq = freq.sort_by {|key, val| key}
```

```ruby
# MATH OPERATIONS
2 + 2		# addition
2 - 4		# subtraction
2**3	 	# potenzbildung
2/3			# dividing (integer)
2.0/3		# dividing (float numbers)
36 % 6	# modulo: remainder = 0
37 % 6  #         remainder = 1
"Hello," << " world" << "!"   # concatenation operator (SHOVEL)

.round(n)		# round with given precision precision (n = how many decimal places)
2.342.round  	# = 2
2.342.round(2) 	# = 2.34
.ceil			
2.342.ceil		# = 3
.floor
2.342.floor		# = 2
```


```ruby
# SYMBOLS
.object_id		# gets the id of an object
:string 		# symbol "called" "string". starts with ":"
p :string.object_id == :string.object_id	# true
p "string".object_id == "string".object_id 	# false

.to_s		# converting symbol (or other types) to string
.to_sym		# conversion to symbol
.intern		# conversion to symbol (other variation doing the same thing)
```


