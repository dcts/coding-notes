# Ruby Shoes

- library to create canvases (similar to JFrame in java)

```ruby
# basic app
Shoes.app(title: "myApp") do
  # todo
end

# stack (VERTIKAL)
stack(margin: 10) do 	# do something
end

# flow (HORIZONTAL)
flow(margin: 10) do 	# do something
end

# button
button("button label")

# paragraph
para("this is a paragraph")

# caption
caption("TITLE! (displayed bold and big)", margin: 10)



# info pane (OK)
alert("Hi, im an alert! You can only click OK to make me disappear!")

# get user input (OK | CANCEL)
my_name = ask("Please, enter your name:")	# stores input in variable name

# colorpicker tool lets user pick a color
my_color = ask_color("Pick a background")	# stores color in variable my_color
Shoes.app {background my_color}

# get content of a file
filename = ask_open_file
Shoes.app do
  para File.read(filename)
end
```