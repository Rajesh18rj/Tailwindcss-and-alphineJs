# 1

flex kudutha , antha container la irukathulam straight line ku vanthuduthu.. 

for example 

a
b

ipdi thani thaniya irukunaa.. flex kuduthathum

a b 

ipdi aagiduthu.. 

------------------------------------------------------------------------------------------------------------------------
items-center

now <flex item-center> nu kuduthathum, hight wise la center ku varuthu.. 

then 
  <flex justify-center
nu kuduthaa, 

height wise center ku pogama , width wise top of the center ku poguthu.. 

then
   <flex justify-center items-center>
nu kuduthaa, width oda center of the center poguthu.. 

< flex items-center justify-between>
intha mari kudutha items laam height wise center poi.. 
div kulla ippo rendu content iruku ..

 onnu <p>Awesome</p>
 innonu <p> Navigation </p>

intha mari iruntha rendum height wise center poi, onnu right corner , another one left corner pogiduthu.. 

lets come to nav section

<nav>
    <ul class="flex items-center ">
        <li> <a class="p-4 hover:bg-gray-700 rounded-lg" href="">Home</a> </li>
        <li><a class="p-4 hover:bg-gray-700 rounded-lg" href="">Create Post</a></li>
        <li><a class="p-4 hover:bg-gray-700 rounded-lg" href="">Bart</a></li>

    </ul>
</nav>

intha mari ovoru list ku thani thaniya class yeluthurathuku bathila, 

<nav>
    <ul class="flex items-center [&>li>a]:p-4 [&>li>a]:hover:bg-gray-700 [&>li>a]:rounded-lg ">
        <li> <a  href="">Home</a> </li>
        <li><a  href="">Create Post</a></li>
        <li><a  href="">Bart</a></li>

    </ul>
</nav>
 ipdi yeluthalam.. 

         then itha inga yelutha venam style tag kulla yeluthanum nu nenacha 

<style type="text/tailwindcss">
    .navitems {
        @apply [&>li>a]:p-4 [&>li>a]:hover:bg-gray-700 [&>li>a]:rounded-lg
    }
</style>

intha mari styles la yelutha athoda name ah class la kudukalam 
<nav>
    <ul class="flex items-center navitems ">                 #we give that name (navitems)
        <li> <a  href="">Home</a> </li>
        <li><a  href="">Create Post</a></li>
        <li><a  href="">Bart</a></li>

    </ul>
</nav>

ipdi kuduthalum wrk aaagumm.. 

intha style ah innum kooda short panlam.. 

<style type="text/tailwindcss">
    .navitems>li>a {
        @apply p-4 hover:bg-gray-700 rounded-lg
    }
</style>
intha maari.. 
