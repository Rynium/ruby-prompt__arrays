---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

An array is a data object that stores ordered lists.



# What are some examples of information that would be Arrays as opposed to some other data type?

Examples of arrays could be any mix of numbers, strings, objects, or even arrays themselves. 



# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?

We can retrieve elements in an array in the same way that we retrieve elements in a string.
    array = [ 1,2,3,4,5,6,7,8,9]
    puts array[8]     # this would give us the number "9", which is our 9th element. If we wanted to find the 8th element, we could use array[7].
If we try to retreive a number that doesn't exist in an array. We will get a "nil" value. 



# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

Negative numbers can be used to retrieve data from an array. Say we wanted to retrieve the last value of our array, we could use array[-1] to access this. If we wanted to access the second to last, we could do so with array[-2]. This patter contunes on up until the index of array[-array.length], which would access the same item as array[0].
    array = [ 1,2,3,4,5,6,7,8,9]
    puts array[-9]    # give us the number "1". Any index value below -9 would return a "nil" value.



# How would you perform an operation on every element inside an Array?

A loop could be used to iterate through every index in an array. For instance if we wanted to double ever number in an array, we could use the following loop.
   array = [ 1,2,3,4,5,6,7,8,9]
   array.each {|n| puts n*2}   #This puts each number multiplied by two onto the screen with each being on a different line. It does not alter array in any way, it just simply puts the value multiplied by two to the screen!



# How do you add elements to an Array?

Elements can be added to the end of an array by using the ".push()" method.
    array = [ 1,2,3,4,5,6,7,8,9]
    array.push(10)   #    array = [ 1,2,3,4,5,6,7,8,9,10]
Elements can be added anywhere in the array using the ".insert(index, item to be inserted)" method.
    array = [ 1,2,3,4,5,6,7,8,9]
    array.insert(0, "0")   #    array = ["0",1,2,3,4,5,6,7,8,9]
Elements can be removed from the end of the array and returned using the ".pop" method.
    arrary = [1,2,3,4,5]
    array.pop     #  array = [1,2,3,4]
Elements can be removed from any index using the ".delete_at(index)" method.
    array = [1,2,3,4,5]
    array.delete_at(2)    #   array = [1,2,4,5]



# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

  Using the follow code would replace the item at index 1 of this array, replacing "Fiona" with "Florence" 
         names[1].replace("Florence")
  
  If we don't know whether "Fiona' exists or not, we can use our ".map"(because this returns a new array vs ".each" wichi returns the oringal array) to iterate through each value to check "if" it is equal to "Fiona", and then replacing it with "Florence if that is true:
        array.map! do |x|
            if x == 'Fiona'
                'Florence'
            else
                x
            end
        end

# What do the methods `push`, `pop`, `shift`, and `unshift` do?
    "push" will add an item on to the end of an array.  
    "pop" will remove an item from the end of an array.
    "shift will add an item on to the front of an array.
    "unshift" will remove the first item from an array.



# How do you determine how many elements are in an Array?

    array_name.length will tell you the number of items located in an array.



# How would you reverse the order of elements in an Array?

     array_name.reverse will reverse the order of items in an array.
     
     
     
# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

To take a string "Sumeet Jain" and return the names split up, we could use the code below to return an array with 2 items.
    name = "Sumeet Jain"
    name_array = name.split(" ")    # name_array = ["Sumeet","Jain"]
To take a string "Sumeet Jain" and return the letters split up, we could do the following.
    name = "Sumeet Jain"
    name_array = name.split("")    
To take ["S","u","m","e","e","t"] and turn it into a string "Sumeet" we could use the ".join(separator)" method.
    array =  ["S","u","m","e","e","t"]
    string = array.join("")  # this sets string equal to "Sumeet"
