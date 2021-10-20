process.stdin.resume();
process.stdin.setEncoding('utf8');

// your code goes here

function  isfromValid(firstName,lastName,email,phone,message){
    var phoneno = /^\d{10}$/;
    var newphoneno = /^\+?([0-9]{2})\)?[-. ]?([0-9]{4})[-. ]?([0-9]{4})$/;
    var regName = /^[a-zA-Z]+ [a-zA-Z]+$/;
    
    
var mailformat = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
  var c=0;
  if(phoneno.test(phone) )
        {
            return true;
       
        }else{
            console.log("phone not 10");
            return false;
        }
        if(newphoneno.test(phone))
        {
            return true;
       
        }else{
            console.log("phone not good");
            return false;
        }
        if(mailformat.test(email))
        {
            return true;
       
        }else{
            console.log("phone not mail");
            return false;
        }
        if(regName.test(firstName))
        {
            return true;
       
        }else{
            console.log("phone not firstname");
            return false;
        }
        if(regName.test(lastName))
        {
            return true;
       
        }else{
            console.log("phone not lastname");
            return false;
        }
        
    return false;
}


let valid=isfromValid("","mohan","er.@.com",1234567890,"notanki");
console.log(valid);
