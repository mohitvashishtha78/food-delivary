<!DOCTYPE html>
<html>
    <head>
        <style>
            tr{
                background-color: mediumaquamarine;
                color: black;
                text-align: center;
            }
            dt{
                font-weight: bold;
                background-color: mediumaquamarine;
                color: black;
            }
        </style>
         <script>
             function placeorder(){
                 document.getElementById("order summary").style.display="block";

                 Uname=document.getElementById("txtname");
                 mobile=document.getElementById("txtmob");
                 burger=document.getElementById("optburger");
                 momos=document.getElementById("optmomos");
                 drink=document.getElementById("optdrink");

                var mcost=0;
                var acost=0;
                var mname= " ";
                var aname= " ";
                if(burger.checked){
                    mcost=125;
                    mname=burger.value;
                }
                if(momos.checked){
                    mcost=80;
                    mname=momos.value;
                }
                if(drink.checked){
                    acost=40;
                    mcost += acost;
                    aname += drink.value+ "<br>" ;

                }
                document.getElementById("lblname").innerHTML=Uname.value;
                document.getElementById("lblmob").innerHTML=mobile.value;
                document.getElementById("lblmeal").innerHTML=mname;
                document.getElementById("lbladd").innerHTML=aname;
                document.getElementById("lblamount").innerHTML= mcost;

             }
         </script>

    </head>
    <body>
        <font size="6">
            <table width="800" border="2" cellspacing="4" cellpadding="4" align="center" id="orderform">
                <tr>
                    <td>
                        <img src="fast food.jpg" width="300" height="300">
                    </td>
                </tr>
                <tr>
                    <td colspan="2">Customer Details</td>
                </tr>
                <tr>
                    <td>Customer Name</td>
                    <td>
                        <input type="text" id="txtname">
                    </td>
                </tr>
                <tr>
                    <td>Customer mobile no.</td>
                    <td>
                        <input type="text" id="txtmob">
                    </td>
                </tr>
                <tr>
                    <td>select a meal</td>
                </tr>
                <tr>
                    <td>
                        <img src="burger.jpg" width="100" height="100">
                        <br>
                        <input type="radio" name="meal" id="optburger" value="omgburger">omgburger(&#8377;125/-)
                    </td>
                    <td>
                        <img src="momos.jpg" width="100" height="100">
                        <br>
                        <input type="radio" name="meal" id="optmomos" value="omgmomos">omgmomos(&#8377;80/-)
                    </td>
                </tr>
                <tr>
                    <td colspan="2">
                        select Ad-on's
                    </td>
                </tr>
                <tr>
                    <td>
                        <img src="drink.jfif" width="100" height="100">
                        <br>
                        <input type="checkbox" id="optdrink" value="can">can(&#8377;40/-)
                    </td>
                </tr>
                <tr>
                    <td>
                        <input type="button" value="Place Order" onclick="placeorder()">
                    </td>
                </tr>

            </table>
            <br>
            <dl id="order summary" style="display: none;">
                <h2>Order Summary</h2>
                <dt>Customer Name</dt>
                <dd id="lblname"></dd>
                <dt>Mobile</dt>
                <dd id="lblmob"></dd>
                <dt>Meal</dt>
                <dd id="lblmeal"></dd>
                <dt>Ad-On's</dt>
                <dd id="lbladd"></dd>
                <dt>Total bill Amount</dt>
                <dd id="lblamount"></dd>
                <br>
                <input type="button" value="print bill" onclick="window.print()">
            </dl>
    </body>
</html>
