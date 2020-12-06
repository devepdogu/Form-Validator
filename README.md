# Form-Validator 
 Control all of the input in project / With form tag or without form tag
 
- > Usage  --  $validator(selector,config)
- > If you add input attribute data-error-name error exp : <code>&lt;input type="text" data-error-name="First Name" &gt;</code> error like this giving : First Name is required
 
# With Form Tag
  - must be give form tag <code>id</code> or <code>class</code> exp : <code><form class='valid'&gt;</code>
 
  - add <code>&lt;script&gt;</code> and call the <code>$validator('.valid');</code> after <code>jquery,validator.min.js</code>
 
  - its done :)
  -  ![form](https://user-images.githubusercontent.com/48163490/101239012-5cfe7700-36f5-11eb-8892-bd339df2e6db.png)

# Without Form Tag
  - must be give which control input add  <code>id</code> or <code>class</code> exp : <code><input type="email" class="form-control valid"&gt; </code>
  
  - add <code>&lt;script&gt;</code> and call the <code>$validator('.valid');</code> after <code>jquery,validator.min.js</code>
 
  - dont forget add clickSelector in config  <code>$validator('.valid',config)</code>  clickSelector mean which element clicked control the input  
  #Usage <code>$validator('.valid',{  clickSelector:".btn" }) </code>
  
  - its done :)
  - ![withoutform](https://user-images.githubusercontent.com/48163490/101239179-8a97f000-36f6-11eb-90b9-ed2e45bba4e6.png)

  

 
 # Config

 - theme: <code>Default Value = "danger"</code> &nbsp;  <code>"primary","secondary","success","danger","warning","info","dark"</code>
  
   - > <code> Usage $(selector,{ theme:"warning" });</code>
  
 - icon: <code>Default Value = "fas fa-exclamation-circle"</code>  <code>Every icon !!Which use icons template you must be include the project</code> 

   - > <code> Usage $(selector,{ icon:"fas fa-smile-wink" });</code>
  
 - captcha: <code>Default Value =null </code> 
   - > <code> Usage $(selector,{ captcha:true });</code>
   - > CUSTOMIZE CAPTCHA <code> captchaType:"all" , captchaLength:5 , className:"form-control" , id:null , captchaInside:null</code>
       - > captchaType : <code>Captcha password type</code> <code>"all","number","letter"</code>
           - > <code> Usage $(selector,{ captcha:{  captchaType:"number" } });</code>
       - > captchaLength : <code>Captcha password length</code> 
           - > <code> Usage $(selector,{ captcha:{  captchaLength:6 } });</code>
       - > className : <code>Captcha class name</code> 
           - > <code> Usage $(selector,{ captcha:{  className:"captcha-class" } });</code>
       - > captchaInside : <code>Captcha add inside giving value (id or class) !!If you dont give this parameter Captcha auto add before clickSelector or form [type=submit] </code> 
           - > <code> Usage $(selector,{ captcha:{  captchaInside:"#captcha-wrap" } });</code>
   
   
 - text: <code> All input[type=text]  setting </code>  
   - >  minLength : <code> Default Value = 2</code> &nbsp; <code>Usage $(selector, {  text:{ minLength:10 }  }  )</code>
   - >  maxLength : <code> Default Value = 40</code> &nbsp; <code>Usage $(selector, {  text:{ maxLength:100 }  }  )</code>
   - >  notHaveSpecailCase : <code> Default Value = false</code> &nbsp; <code>input[type=text] not contain special case</code>
        - > <code>Usage $(selector, {  text:{ notHaveSpecailCase:true }  }  )</code>  
   - >  notHaveNumberCase : <code> Default Value = false</code> &nbsp; <code>input[type=text] not contain number </code>
        - > <code>Usage $(selector, {  text:{ notHaveNumberCase:true }  }  )</code>
   - >  messages : 
        - > isEmpty : <code> Default Value = "This field is required" </code> &nbsp;
            - <code>Usage $(selector, {  text:{ messages:{  isEmpty : "its Empty"  } }  }  )</code>
            
        - > isMaxOrMinLength : <code> Default Value = "This field must be  2-40 characters " </code> &nbsp;
            - <code>Usage $(selector, {  text:{ messages:{  isMaxOrMinLength : "No way!"  } }  }  )</code>
            
        - > isNotHaveSpecailCase : <code> Default Value = "This field cannot be contain with a special character " </code> &nbsp;
            - <code>Usage $(selector, {  text:{ messages:{  isNotHaveSpecailCase : "its Empty"  } }  }  )</code>
            
        - > isNotHaveNumberCase : <code> Default Value = "This field cannot be contain with a number " </code> &nbsp;
            - <code>Usage $(selector, {  text:{ messages:{  isNotHaveNumberCase : "No way!"  } }  }  )</code>
            
- password: <code> All input[type=password]  setting </code>  
   - >  minLength : <code> Default Value = 5</code> &nbsp; <code>Usage $(selector, {  password:{ minLength:10 }  }  )</code>
   - >  maxLength : <code> Default Value = 20</code> &nbsp; <code>Usage $(selector, {  password:{ maxLength:100 }  }  )</code>
   - >  haveSpecialCase : <code> Default Value = false</code> &nbsp; <code>input[type=password] must be contain special char </code>
        - > <code>Usage $(selector, {  password:{ haveSpecialCase:true }  }  )</code>
   - >  haveUpperCase : <code> Default Value = false</code> &nbsp; <code>input[type=password] must be contain a uppercase letter</code>
        - > <code>Usage $(selector, {  password:{ haveUpperCase:true }  }  )</code>
   - >  haveNumberCase : <code> Default Value = false</code> &nbsp; <code>input[type=password] must be contain a number </code>
        - > <code>Usage $(selector, {  password:{ haveNumberCase:true }  }  )</code>
   - >  haveLowerCase : <code> Default Value = false</code> &nbsp; <code>input[type=password] must be contain a lowercase letter</code>
        - > <code>Usage $(selector, {  password:{ haveLowerCase:true }  }  )</code>
   - >  justNumberCase : <code> Default Value = false</code> &nbsp; <code>input[type=password] must be contain just number </code>
        - > <code>Usage $(selector, {  password:{ justNumberCase:true }  }  )</code>
   - >  showRules : <code> Default Value = false</code> &nbsp; <code>This property add after password input show how must be if value giving true dont show errors </code>
        - > <code>Usage $(selector, {  password:{ showRules:true }  }  )</code>
   - >  showPassword : <code> Default Value = false</code> &nbsp; <code>This property add in input password the eye icon if eye clicked show the password </code>
        - > <code>Usage $(selector, {  password:{ showPassword:true }  }  )</code>
   - >  repeatPassword : <code> Default Value = false</code> &nbsp; <code>This property add after input password re-type password </code>
        - > <code>Usage $(selector, {  password:{ repeatPassword:true }  }  )</code>
   - >  messages : 
        - > isEmpty : <code> Default Value = "This field is required" </code> &nbsp;
            - <code>Usage $(selector, {  password:{ messages:{  isEmpty : "its Empty"  } }  }  )</code>
            
        - > isMaxOrMinLength : <code> Default Value = "This field must be  5-20 characters " </code> &nbsp;
            - <code>Usage $(selector, {  password:{ messages:{  isMaxOrMinLength : "No way!"  } }  }  )</code>
            
        - > isHaveSpecialCase : <code> Default Value = "This field must be contain with a special character" </code> &nbsp;
            - <code>Usage $(selector, {  password:{ messages:{  isHaveSpecialCase : "No way!"  } }  }  )</code>
        
        - > isHaveUpperCase : <code> Default Value = "This field must be contain with a uppercase letter" </code> &nbsp;
            - <code>Usage $(selector, {  password:{ messages:{  isHaveUpperCase : "No way!"  } }  }  )</code>
            
        - > isHaveNumberCase : <code> Default Value = "This field must be contain with a number " </code> &nbsp;
            - <code>Usage $(selector, {  password:{ messages:{  isHaveNumberCase : "No way!"  } }  }  )</code>
            
        - > isHaveLowerCase : <code> Default Value = "This field must be contain with a lowercase letter " </code> &nbsp;
            - <code>Usage $(selector, {  password:{ messages:{  isHaveLowerCase : "No way!"  } }  }  )</code>
            
        - > isJustNumberCase : <code> Default Value = "This field must be only contain with numbers " </code> &nbsp;
            - <code>Usage $(selector, {  password:{ messages:{  isJustNumberCase : "No way!"  } }  }  )</code>
         
        - > isNotMatch : <code> Default Value = "Passwords not match " </code> &nbsp;
            - <code>Usage $(selector, {  password:{ messages:{  isNotMatch : "No way!"  } }  }  )</code>

- email: <code> All input[type=email]  setting </code>  
   - >  minLength : <code> Default Value = 5</code> &nbsp; <code>Usage $(selector, {  email:{ minLength:10 }  }  )</code>
   - >  maxLength : <code> Default Value = 120</code> &nbsp; <code>Usage $(selector, {  email:{ maxLength:100 }  }  )</code>
   - >  messages : 
        - > isEmpty : <code> Default Value = "This field is required" </code> &nbsp;
            - <code>Usage $(selector, {  email:{ messages:{  isEmpty : "its Empty"  } }  }  )</code>
            
        - > isMaxOrMinLength : <code> Default Value = "This field must be  5-120 characters " </code> &nbsp;
            - <code>Usage $(selector, {  email:{ messages:{  isMaxOrMinLength : "No way!"  } }  }  )</code>
            
        - > isInvalid : <code> Default Value = "The e-mail address is incorrect " </code> &nbsp;
            - <code>Usage $(selector, {  email:{ messages:{  isInvalid : "No way!"  } }  }  )</code>
            
- date: <code> All input[type=date]  setting </code>  
   - >  dateRange : <code> Default Value = null</code> &nbsp;<code> If you want min and max must be giving '|' </code> <code>"today","yesterday","tomorrow","+-x day|week|month|year"</code> <code>This mean just pick the min and max values </code>
        - > <code>Usage $(selector, {  date:{ dateRange:"today|+1 week" }  }  )</code>
   - >  messages : 
        - > isEmpty : <code> Default Value = "This field is required" </code>
            - <code>Usage $(selector, {  date:{ messages:{  isEmpty : "its Empty"  } }  }  )</code>
            
        - > dateRange : <code> Default Value = "The date wrong chosen" </code> 
            - <code>Usage $(selector, {  date:{ messages:{  dateRange : "No way!"  } }  }  )</code>
            
- file: <code> All input[type=date]  setting </code>  
   - >  fileSize : <code> Default Value = 0</code> &nbsp; <code>"xkb|mb"</code>
        - > <code>Usage $(selector, {  file:{ fileSize:"100kb" }  }  )</code>
   - >  fileExt : <code> Default Value = null</code> &nbsp; <code>"x|y|z"</code>
        - > <code>Usage $(selector, {  file:{ fileExt:"gif|png" }  }  )</code>    
   - >  messages : 
        - > isEmpty : <code> Default Value = "This field is required" </code>
            - <code>Usage $(selector, {  file:{ messages:{  isEmpty : "its Empty"  } }  }  )</code>
            
        - > isFileExt : <code> Default Value = "The chosen file extension is wrong" </code> 
            - <code>Usage $(selector, {  file:{ messages:{  isFileExt : "No way!"  } }  }  )</code>
            
        - > isFileSize : <code> Default Value = "The chosen file size is big" </code> 
            - <code>Usage $(selector, {  file:{ messages:{  isFileSize : "No way!"  } }  }  )</code>
            
- number: <code> All input[type=number]  setting </code>  
   - >  Min : <code> Default Value = 1</code> &nbsp; <code>Usage $(selector, {  number:{ Min:1 }  }  )</code>
   - >  Max : <code> Default Value = 100</code> &nbsp; <code>Usage $(selector, {  number:{ Max:100 }  }  )</code>
   - >  messages : 
        - > isEmpty : <code> Default Value = "This field is required" </code> &nbsp;
            - <code>Usage $(selector, {  number:{ messages:{  isEmpty : "its Empty"  } }  }  )</code>
            
        - > isMaxOrMinValue : <code> Default Value = "This field must be between the values 1-100 " </code> &nbsp;
            - <code>Usage $(selector, {  number:{ messages:{  isMaxOrMinValue : "No way!"  } }  }  )</code>
      
      
 - tel: <code> All input[type=tel]  setting </code>  
   - >  minLength : <code> Default Value = 8</code> &nbsp; <code>Usage $(selector, {  tel:{ minLength:1 }  }  )</code>
   - >  maxLength : <code> Default Value = 20</code> &nbsp; <code>Usage $(selector, {  tel:{ maxLength:100 }  }  )</code>
   - >  countryCode : <code> Default Value = null </code> &nbsp; <code>Usage $(selector, {  tel:{ countryCode:"+90" }  }  )</code>
   - >  messages : 
        - > isEmpty : <code> Default Value = "This field is required" </code> &nbsp;
            - <code>Usage $(selector, {  tel:{ messages:{  isEmpty : "its Empty"  } }  }  )</code>
            
        - > isMaxOrMinLength : <code> Default Value = "This field must be  8-20 characters " </code> 
            - <code>Usage $(selector, {  tel:{ messages:{  isMaxOrMinLength : "No way!"  } }  }  )</code>
            
 - textarea: <code> All input[type=tel]  setting </code>  
   - >  minLength : <code> Default Value = 10</code> &nbsp; <code>Usage $(selector, {  textarea:{ minLength:1 }  }  )</code>
   - >  maxLength : <code> Default Value = 120</code> &nbsp; <code>Usage $(selector, {  textarea:{ maxLength:100 }  }  )</code>
   - >  messages : 
        - > isEmpty : <code> Default Value = "This field is required" </code> &nbsp;
            - <code>Usage $(selector, {  tel:{ textarea:{  isEmpty : "its Empty"  } }  }  )</code>
            
        - > isMaxOrMinLength : <code> Default Value = "This field must be  10-120 characters " </code> 
            - <code>Usage $(selector, {  tel:{ textarea:{  isMaxOrMinLength : "No way!"  } }  }  )</code>
     
     
 - constMessages:
   - > isEmpty : <code> Default Value =null </code> &nbsp; <code> If checkbox and select value are empty this property change error message </code>
   - > isCaptchaEmpty : <code> Default Value =null </code> &nbsp; <code> If Captcha value is empty this property change error message </code>
   - > isCaptchaPassWrong : <code> Default Value =null </code> &nbsp; <code> If Captcha value is wrong this property change error message </code>
   - > Usage <code>$validator(selector,{ constMessages:{ isCaptchaEmpty:"Capctha is Empty!" } })</code>
   
   
 - customInput:
   - > If you are dont want the control one input or change property other you must be use this
   - > Must be giving which change element (id or class)
   - > The giving element's property same with unique above 
   - > If you dont control element you must be call NotRequired:true
       - > Usage <code>$validator(selector, customInput:".not_valid":{ NotRequired:true}  ) </code>
   - > This Property must be giving input type "date,number,text,textarea,checkbox"
   
# FUNCTIONS:
 - This property is giving just function!
   - > formValid : <code> Default Value =null </code> &nbsp; <code> If form validation is true you must be calling this property </code>
      - <code>If you call formValid form action attribute not working </code>
      - If you use ajax with form input value must be arrow function !!
        - > <code>formValid return FormData catch the this.FormData </code>
        - > <code>Ajax need the processData: false, contentType:false, property</code>
        - > <code>If add FormData new value this.FormData.append(key,value) </code>
        - > Usage with ajax  
        - ![deneme](https://user-images.githubusercontent.com/48163490/101278997-26e1f580-37d0-11eb-9a40-e4810bc45ffb.png)
  
 - > formLoad : <code> Default Value =null </code> &nbsp; <code>When form load calling the this property </code>
      - <code>Usage $validator(selector,{ formLoad:function() { console.log("Form Loadded Yeyy"); } }); </code>
 
 - > formClick : <code> Default Value =null </code> &nbsp; <code>If you giving clickSelector  clickSelector clicked formClick working else form[type=submit] clicked formClick   working  </code>
      - <code>Usage $validator(selector,{ formClick:function() { console.log("You click me!"); } }); </code>
