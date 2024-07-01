<html>
<head>
	<title>Form Submit</title>
	<style>
        *{
            margin: 0;
            padding: 0;
            font-family: Arial, Helvetica, sans-serif
        }

        body{
            background-color: #98efe1;
        }

        .content{
            text-align: ;
            display: ;
            position: relative;
           
        }

        form{
            display: flex;
			flex-direction: column;
            position: relative;
            overflow: hidden;
            background-color: #eeeeee;
            padding: 20px 30px;
            overflow: hidden;
            width: 345px;
            border-radius: 15px;
            top: 10px;
            border: 1px solid rgb(141, 141, 141);
            top: 30px;
            position: relative;
            
            
            

        }
        label{
            /* left: -90px; */
            text-align: left;
            margin: 10px;
            position: relative;
        }

        input{
            padding: 10px 15px;
            width: 320px;
            margin-bottom: 0px;
            border-radius: 6px;
            border: 1px solid rgb(119, 119, 119);
            display: flex;
            position: relative;
           
            
        }

        .click{
            margin: 10px;
            background-color: rgb(4, 162, 4);
            color: #fff;
            border: none;
            font-size: 15px;
            font-weight: bold;
            padding: 10px 20px;
            border-radius: 6px;
            margin: 5px;
            width: 346px;
            cursor: pointer;

        }

        .click:hover{
            background-color: rgb(5, 134, 5);
        }

        textarea{
            padding: 10px 15px;
            width: 322px;
            height: 50px;
            margin-bottom: 10px;
            border-radius: 6px;
            border: 1px solid rgb(122, 121, 121);
            position: relative;

        }

        .line{
            font-size: 10px;
            color: rgb(33, 33, 33);
            margin: 6px;
        }
	
	</style>
</head>
<body>
	<div class="content">
        <center>
        <form method="post" action="" name="product" id="product">
            <h1>Employee Information</h1>
            
            <label for="name">Name</label>
            <input class="fil" type="text" name="Name" placeholder="Enter Employee Name" required>

            <label for="name">Address*</label>
            <input class="fil" type="text" name="Address" placeholder="Enter Employee address" required>

            <label for="name">Email ID</label>
            <input class="fil" type="text" name="Email" placeholder="Enter employee email id" required>

            <button class="click">Submit &#10132;</button>

        </form>
        </center>
      
    </div>
    <script>
        const scriptURL = 'https://script.google.com/macros/s/AKfycbz8VmSwNdxoXFIaVve4INrHcpwyS2BEoZTtaCMmN1nc0zlFubLgGLnyObq94RI1thMPbw/exec'
        const form = document.forms['product']
      
        form.addEventListener('submit', e => {
          e.preventDefault()
          fetch(scriptURL, { method: 'POST', body: new FormData(form)})
            .then(response => alert("Thank you! your form is submitted successfully." ))
            .then(() => {  window.location.reload(); })
            .catch(error => console.error('Error!', error.message))
        })
      </script>
    <br>
</body>
</html>

