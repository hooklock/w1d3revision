Code  Revisions 1
Raw  arrays_hashes_quiz.md
Array and Hash Questions
Duration 1 hour

A. Given the following data structure:

lines = ['Gyle Centre', 'Edinburgh Park', 'Murrayfield Stadium', 'Haymarket', 'Princes Street']
Work out how many stops there are in the lines array

  lines.length

Return 'Edinburgh Park' from the array

  lines[1]

How many ways can we return 'Princes Street' from the array?

  lines[4]
  lines.last
  lines[-1]
  lines.at(4)

Work out the index position of 'Haymarket'

  lines.index("Haymarket")

Add 'Airport' to the start of the array

  lines.unshift("Airport")

Add 'York Place' to the end of the array

  lines << "York Place"

Remove 'Edinburgh Park' from the array using it's name

  lines.delete "Edinburgh Park"

Delete 'Edinburgh Park' from the array by index

  lines.delete_at(1)

Reverse the positions of the stops in the array

  lines.reverse

Print out all of the stops using loop / while / until / for

FOR LOOP

  for stop in lines
    puts stop
  end
  
LOOP LOOP

  loop do
    puts lines
    break
  end
  
WHILE LOOP

  i = 0
  while i < lines.length
    puts lines[i]
    i += 1
  end
  
UNTIL LOOP

    i = 0
    until i == lines.length
      puts lines[i]
      i+=1
    end

B. Given the following data structure:

  my_hash = {0 => "Zero", 1 => "One", :two => "Two", "two" => 2}

How would you return the string "One"?

  my_hash[1]

How would you return the string "Two"?

  my_hash[:two]

How would you return the number 2?

  my_hash["two"]

How would you add {3 => "Three"} to the hash?

  my_hash[3] = "Three"

How would you add {:four => 4} to the hash?

  my_hash[:four] = 4

C. Given the following data structure:

  users = {
    "Jonathan" => {
      :twitter => "jonnyt",
      :favourite_numbers => [12, 42, 75, 12, 5],
      :home_town => "Stirling",
      :pets => {
        "fluffy" => :cat,
        "fido" => :dog,
        "spike" => :dog
      }
    },
    "Erik" => {
      :twitter => "eriksf",
      :favorite_numbers => [8, 12, 24],
      :home_town => "Linlithgow",
      :pets => {
        "blinky" => :fish,
        "kevin" => :fish,
        "spike" => :dog,
        "fang" => :parrot
      }
    },
    "Anil" => {
      :twitter => "bridgpally",
      :favorite_numbers => [12, 14, 85, 88],
      :home_town => "Dunbar",
      :pets => {
        :colin => :snake
      }
    },
  }

Return Jonathan's Twitter handle (i.e. the string "jonnyt")

  users["Jonathan"][:twitter]

Return Erik's hometown

  users["Erik"][:home_town]

Return the array of Erik's favorite numbers

  users["Erik"][:favorite_numbers]

Return the type of Anil's pet Colin

  users["Anil"][:pets][:colin]

Return the smallest of Erik's favorite numbers

  users["Erik"][:favorite_numbers].min

Return an array of Anil's favorite numbers that are even

  users["Anil"][:favorite_numbers].each { |value| puts value if value.to_f%2==0}

Return an array of Jonathans favourite numbers, sorted in ascending order and excluding duplicates

  users["Jonathan"][:favourite_numbers].sort.uniq

Add the number 7 to Erik's favorite numbers

  users["Erik"][:favorite_numbers].push 7

Change Erik's hometown to Edinburgh

  users["Erik"][:home_town]="Edinburgh"

Add a pet dog to Erik called "Fluffy"

  users["Erik"][:pets][:dog] = "Fluffy"

Add yourself to the users hash

  users["Adam"]={twitter: "hooklock", favorite_numbers: [3,5,9,12,27], home_town: "Glasgow", pets:{"Mack"=>:dog, "Sasha"=>:cat, "Carmen"=>:cat}}
  => {:twitter=>"hooklock", :favorite_numbers=>[3, 5, 9, 12, 27], :home_town=>"Glasgow", :pets=>{"Mack"=>:dog, "Sasha"=>:cat, "Carmen"=>:cat}}