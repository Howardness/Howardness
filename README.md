<!DOCTYPE html>
<!-- Created By CodingNepal -->
<html lang="en" dir="ltr">
   <head>
      <meta charset="utf-8">
      <title>To-Do List | CodingNepal</title>
      <link rel="stylesheet" href="style.css">
      <script src="https://code.jquery.com/jquery-3.4.1.js"></script>
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"/>
   </head>
   <body>
      <div class="center">
         <div class="button">
            <span class="text">To-Do List</span>
            <span class="icon"><i class="fas fa-sort-down"></i></span>
         </div>
         <div class="field">
            <input type="text" required placeholder="Add your new to-do list">
            <span class="add-btn">ADD</span>
         </div>
         <ul>
            <li><span><i class="fa fa-trash"></i></span>Get a new laptop</li>
            <li><span><i class="fa fa-trash"></i></span>Go to shopping</li>
            <li><span><i class="fa fa-trash"></i></span>Read a newspaper</li>
            <li><span><i class="fa fa-trash"></i></span>Go to college</li>
            <li><span><i class="fa fa-trash"></i></span>Buy a new phone</li>
         </ul>
      </div>
      <script>
         $('.add-btn').click(function(){
           $('ul').append("
         <li><span><i class='fa fa-trash'></i></span>"+ $('input').val() +"</li>
         ");
            $('input').val("");
         });
         $('ul').on("click", 'span', function(){
           $(this).parent().fadeOut(500,function(){
             $(this).remove();
           });
         });
         $('.icon').click(function(){
           $('.field').toggleClass("hide");
         })
      </script>
   </body>
</html>
