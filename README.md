# Object oriented program

Its advantages lie in lie in this kind of encapsulation. Here’s a detailed look at some of OOP’s top benefits:

- Modularity for easier troubleshooting

  When working with object-oriented programming languages, you know exactly where to look. “Oh, the car object broke down? The problem must be in the Car class!” You don’t have to muck through anything else.

  That’s the beauty of encapsulation. Objects are self-contained, and each bit of functionality does its own thing while leaving the other bits alone. Also, this modality allows an IT team to work on multiple objects simultaneously while minimizing the chance that one person might duplicate someone else’s functionality.

- Reuse of code through inheritance  
  
  the inheritance technique saves time: Create one generic class (for instance :Car), and then define the subclasses (RaceCar and Limousine) that are to inherit the generic class’s traits.
  your inheriting classes can simply reuse existing code instead of writing these functions all over again.
  another advantage of the OO approach. Simply make a change to your Car class, and all car objects will simply inherit the new code.

- Flexibility through polymorphism

  When a instance of a class can have a unique method or can reproduce the parent class method.

- Effective problem solving

  Object-oriented programming is often the most natural and pragmatic approach, once you get the hang of it. OOP languages allows you to break down your software into bite-sized problems that you then can solve — one object at a time.

## What does this Application Do?

The application is a Books inventory. It will show a list of books, in a distinct category with a price. This Application allows users to Views the list, create or add new books to the existing list (database), update or edit a rows data and delete the data (the entire row).
Every transaction will affect an Array of JSON objects, a temporary database.

## Pseudocode

```html
<html>
<title>CRUD APPLICATION - BOOK_INVENTORY</title>
<body>
<div class="container"></div>
</body>
</html>
```
```javascript
Var myCrudApp equal new function () 


This.myBooks = [{id},{name},{category} ]; 


This.category = [bookcategory1, bookcategory2,… ]    


This.createTable = function(){ loop}


This.col []

Var table=document.createElement(table)  

Table.attributes(id,bookstable)
Var tr=table.insertrow(-1)

For loop thru this.col.length
var th=document.createElement(‘th’)
th.innerHtml=this.col[loopIndex]
tr.appendchild(th)


For loop thru this.myBooks.length (loopindex=i)
Var tr=table.insertrow(-1)
For loop thru this.col.length(loopindex=j)
Var cell=tr.insertcell(-1)
Cell.innerHTML=this.myBooks[i].this.col[j]
This.td=document.createElement(‘td’)
Var lblcancel=document.createElement(‘label’);
Lblcancel.innerHtml=’X’
Lblcancel.setAttribute(‘onclick’,’myCrudApp.cancel(this)’)
Var btnSave=document.createElement(‘input’);
btnSave.setAttribute(‘type’,’button’);
btnSave.setAttribute(‘onclick’,’myCrudApp.Save(this)’)
Var btnUpdate=document.createElement(‘input’);
btnUpdate.setAttribute(‘type’,’button’)
btnUpdate.setAttribute(‘onclick’,’myCrudApp.Update(this)’)
Var btnDelete=document.createElement(‘input’);
btnDelete.setAttribute(‘type’,’button’)
btnDelete.setAttribute(‘onclick’,’myCrudApp.Delete(this)’)

var tr=table.insertrow(-1)
for loop thru this.col.length(loopindex=p)
var newcell=tr.insertcell(-1);
if(p big or equal 1)
        if(p equal 2)
           var select=document.createElement(‘select’)
for loop thru this.category.length(loopindex=k)
select.innerHtml=<option>this.category[k]</option>}
newcell.appendchild(select)
 else
Var tbox=document.createElement(‘textbox’)
Newcell.appendchild(tbox)
This.td=document.createElement(‘td’)
tr.appendchild(This.td)

Var newBtn=document.createElement(‘input’)
newBtn.setAttribute(‘type’,’button’);
newbtn.setAttribute(‘onclick’,’myCrudApp.Create(this)’)
var myDiv=document.getElementById(‘container’)
myDiv.innerHtml=””
myDiv.appendchild(table)
***START OF OPERATIONS***
//CANCEL
This.cancel = function(abutton){
//hide abutton
abutton.setAttribute(‘style’,‘display:none;’)
Var activerow=abutton.parentNode.parentNode.rowindex
//hide the save button
Var saveBtn=document.getElementbyId(‘Save’+(activerow-1))
saveBtn.setAttribute(‘style’,‘display:none;’)
// show the update button again
Var UpdateBtn= document.getElementbyId(‘Edit’,(activerow-1))
UpdateBtn.setAttribute(‘style’,‘display:block;’)
Var tab=document. document.getElementbyId(‘booksTable’).rows[activerow]
For loop thru this.col.length(loopindex=i){
Var td=tab.getElementsBy Tagname(‘td’)[i]
td.innerHtml=this.myBooks[(activerow-1)][this.col[i]];}
//EDIT DATA
This.Update=function(abutton){
Var activerow=abutton.parentNode.parentNode.rowindex
Var tab=document. document.getElementbyId(‘booksTable’).rows[activerow]
//show a dropdown list with a list of categories
For loopthru 4(loopindex=i)
If(i equal 2)
Var td=tab.getElementsByTagname(‘td’)[i]
Var element=document.createElement(‘select’) //dropdown list
Element.innerHtml=<option>td.innertext</option>
For loop thru this.category.length(loopindx=p){
Element.innerHtml= Element.innerHtml +<option>this.category[p]</option>
                                                    
td.innertext=””
td.appendchild(element)
Else 
Var td=tab.getElementsByTagname(‘td’)[i]
Var element=document.createElement(‘input’)
Element.setAttribute(‘type’,’text’)          // text
td.innertext=””
td.appendchild(element)
}
Abutton.setAttribute(‘style’,’display:none’)

//DELETE DATA
This.Delete=function(abutton){
Var activerow=abutton.parentNode.parentNode.rowindex
This.myBooks.splice((active-1),1);//delete the active row
This.createTable() //refresh the table
}
//SAVE DATA
This.Save=function(abutton){
Var activerow=abutton.parentNode.parentNode.rowindex
Var tab=document.getElementById(‘booksTable’).rows[activerow]
//update mybooks array with values
For loop thru this.col.length(loopindex=j)
Var td=tab.getElementsByTagName(‘td’)[j]
If(td.childnodes[0].getAttribute(‘type’) equal ’text’ OR td.childnodes[0].tagName equal ’select’)
//check if element is text or select
This.myBooks[(activerow-1)][this.col[j]]=td.childnodes[0].value //save value
This.createTable() //refresh the table
}
//CREATE NEW
This.createNew=function(abutton){
Var activerow=abutton.parentNode.parentNode.rowIndex
Var tab=document.getElement(‘booksTable’).rows[activerow]
Var myObj={}
//Add new value to  myBooks Array
For loop thru this.col.length(loopIndex=I,start of iteration i=1)
Var td=tab.getElementsByTagname(‘td’)[i]
If(td.childNodes[0].getAttribute(‘type’) equal ‘text’ Or td.childNodes[0].tagname equal ‘select’)
//Check if element is text or select
Var txt=td.childNodes[0].value
If(txt isNot Empty)
myObj[this.col[i]] equal txt.trim()
else
myObj is Empty
alert (‘Please write something!’)
stop
myObj[this.col[0] equal this.myBooks.length incremented by 1//new id
if(Object.keys(myObj).length>0 )//Check if myObj IS NOT empty
this.myBooks.push(myObj) //Add data TO JSON Array
this.createTable() //refresh the table
***OPERATIONS END
myCrudApp.createTable();
```

  
  


