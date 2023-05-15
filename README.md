# HTMLGsheet
This repository will guide you on how to attach or use google sheet as your database for a simple HTML form
This can also Guide you on how to generate PDF of latest entry made on that same google sheet it is done using Js library JSPDF using NodeJs 

Steps To add Google shhet to your HTML Form:
Step1:
First of all go to your html code and in the form section change the name of input type as name="data[name]" as it is going to input the data that user will enter. 
**IMPNote: Do this for all the input labels inside input type

Step2:
Then create a google sheet add the data parameters of your form in sequence that you have in your form.

Step3:
Now go to the sheetdpapi, sign in with your Google account give it all the permissions and click on create new api. Then paste the url of your Google sheet their which will create a new api and generate a link. 
Copy that to your clipboard.

Step4:
Now again in your form section add following things as is:
<form action="api url(fromclipboard)" method="post" id= "sheetdb-form"-submit> -----</form>
Then copy the following code:
 
 <script>
                                    var form = document.getElementById('sheetdb-form');
                                form.addEventListener("submit", e => {
                                  e.preventDefault();
                                  fetch(form.action, {
                                      method : "POST",
                                      body: new FormData(document.getElementById("sheetdb-form")),
                                  }).then(
                                      response => response.json()
                                  ).then((html) => {
                                  
                                    window.open('pass.html', '_blank');
                        
                                  });
                                });
                                
 </script>
 
 Step5:
 DONE.
 
 
 
                               
                              
