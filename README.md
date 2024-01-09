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


 Output:
 
![index](https://github.com/raunakmankapure/Bus-pass-registration-system-for-college/assets/113294200/0c464286-80e1-415a-9a61-36bbbef9adb0)
![2](https://github.com/raunakmankapure/Bus-pass-registration-system-for-college/assets/113294200/45006d25-7787-434f-ba7e-9982871d421b)
![3](https://github.com/raunakmankapure/Bus-pass-registration-system-for-college/assets/113294200/88e320d1-c555-4432-bde2-f23a338f5a38)
![4](https://github.com/raunakmankapure/Bus-pass-registration-system-for-college/assets/113294200/c8265834-4b42-4f0e-a514-31e6acfdb963)
![5](https://github.com/raunakmankapure/Bus-pass-registration-system-for-college/assets/113294200/957a86a5-075c-45c9-9509-216c974b9aef)
![6](https://github.com/raunakmankapure/Bus-pass-registration-system-for-college/assets/113294200/c2f8e6ed-789c-42a9-9a00-bbc10837cbcf)
![index](https://github.com/raunakmankapure/Bus-pass-registration-system-for-college/assets/113294200/7aec8205-7dbc-43f7-ba19-55665dde41cb)
