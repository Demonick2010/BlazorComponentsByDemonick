Alert Component:  
**1. Add the component in Shared or another folder**  
**2. Add the CSS file in wwwroot/css and include in _Host.cshtml** _(e.g. link href="css/demonick_toast.css" rel="stylesheet" )_  
**3. Add image folder in wwwroot/demonick_toast_images**  
**4. Add the component in page** _(e.g. <AlertComponent @ref="@alert" />)_  
**5. Initialize AlertComponent class** _(e.g. AlertComponent alert; )_  
**6. Use calling method for showing alert**  
_(e.g.  
protected override void OnAfterRender(bool firstRender)  
    {  
        if (firstRender)  
        {  
            alert.ChooseMessageWithStatusCode(1, "Header message", "Body message");  
**or**  
            alert.SuccessfulMassage("Header message", "Body message");  
**or**  
            alert.ErrorMassage("Header message", "Body message");  
**or**  
            alert.WarningMassage("Header message", "Body message");  
        }  
    })_  

**Status codes:**  
1 - Successful message alert  
2 - Warning message alert  
3 - Error message alert  
