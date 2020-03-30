# goormProblem
https://stackoverflow.com/questions/60922685/why-do-i-get-empty-string-from-req-body-newitem?noredirect=1#comment107784555_60922685

I posted my Todolist App(from Colt's lecture on Udemy) on Goorm and everything works just fine except one thing.

I tried to make a POST method so that if you press enter it goes to /addItem and creates and add new <li> to the body.

that unfortunately doesn't work and i just get this:

{ newItem: '' }
I compared it to PostRequestDemo that Colt did and it's almost the same code, here:

Mine

app.post("/newItem", function(req,res){
    var newItem = req.body.newItem
    console.log(newItem)     #here is where i get the empty string... it should print something i inputed to the form (for example "banana")
       res.redirect("/")
})   
---------------------
    <form action="/newItem" method="POST"> 
        <input type="text" name="newItem" placeholder="Add New Todo">
    </form>
Colt's

app.post("/addFriend", function(req, res){
    var newFriend = req.body.newFriend
    friends.push(newFriend)
    res.redirect("friends")
})
---------------------
<form method="POST" action="/addFriend">
    <input type="text" name="newFriend" placeholder="Name" required>
    <button>Submit</button>
</form>
if you need more code just let me know bum I'm very very confused because I just started using goorm and express and all of that
