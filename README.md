block.rb
========
def execute(&block)
	block
end

execute { puts "hello, from inside the execute method" }

#nothing prints out

def execute(&block)
	block.call
end
execute { puts "hello, from inside the execute method" }



def execute(block)
	block
end

execute { puts "hello, from inside the execute method"}

#this brings up the error because of the lack of the "&" in front of
#block. it tells us that the argument is a block.
