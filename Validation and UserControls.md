# Validation Controls in ASP.NET

An important aspect of creating ASP.NET Web pages for user input is to be able to check that the information users enter is valid. ASP.NET provides a set of validation controls that provide an easy-to-use but powerful way to check for errors and, if necessary, display messages to the user.

There are six types of validation controls in ASP.NET <br>
<br>
1.RequiredFieldValidation Control <br>
2.CompareValidator Control<br>
3.RangeValidator Control<br>
4.RegularExpressionValidator Control<br>
5.CustomValidator Control<br>
6.ValidationSummary<br>

### 1. RequiredFieldValidation Control
- The RequiredFieldValidator control is simple validation control, which checks to see if the data is entered for the input control.

```C# 
// Syntax
 <div class="form-group">                        
         <asp:Label runat="server">User Name:</asp:Label>
        <asp:TextBox runat="server" class="form-control col-4" ID="usr" name="username"></asp:TextBox>
         <asp:RequiredFieldValidator ID="RequiredFieldValidator1"  runat="server" ErrorMessage="Enter User Name" ControlToValidate="usr"></asp:RequiredFieldValidator>
 </div>

```

### 2. CompareValidator Control<br>
- The CompareValidator control allows you to make comparison to compare data entered in an input control with a constant value or a value in a different control.
 
- It can most commonly be used when you need to confirm password entered by the user at the registration time. The data is always case sensitive.

```C# CompareValidator Control<br>
// Syntax
 <div class="form-group">
   <asp:Label runat="server" for="pwd">Password:</asp:Label>
    <asp:TextBox runat="server" TextMode="Password" class="form-control col-4" ID="pwd" name="passwd"></asp:TextBox>
 </div>

<div class="form-group">
     <asp:Label runat="server" for="rep_pwd">Repeat Password:</asp:Label>
      <asp:TextBox runat="server" type="password" class="form-control col-4" ID="rep_pwd" name="passwd"></asp:TextBox>
      <asp:CompareValidator ID="CompareValidator1" runat="server" ErrorMessage="Password Does not match" ControlToValidate="rep_pwd" ControlToCompare="pwd"></asp:CompareValidator>
 </div>

```

### 3. RangeValidator Control<br>
- The RangeValidator Server Control is another validator control, which checks to see if a control value is within a valid range. 
 
- The attributes that are necessary to this control are: MaximumValue, MinimumValue, and Type.

```C# CompareValidator Control<br>
// Syntax
 <div class="form-group">
      <asp:Label runat="server" for="salary">Expected salary</asp:Label>
      <asp:TextBox runat="server" class="form-control col-4" ID="salary" name="passwd"></asp:TextBox>
      <asp:RangeValidator ID="RangeValidator1" runat="server" ErrorMessage="Enter betwn 100 to 500" ControlToValidate="salary" MaximumValue="500" MinimumValue="100" Type="Integer"></asp:RangeValidator>
 </div>
```

### 4. RegularExpressionValidator Control
- Using RegularExpressionValidator server control, you can check a user's input based on a pattern that you define using a regular expression.
 
- It is used to validate complex expressions. These expressions can be phone number, email address, zip code and many more. Using Regular Expression Validator is very simple. Simply set the ValidationExpression property to any type of expression you want and it will validate it.

```C# CompareValidator Control<br>
// Syntax
 <div class="form-group">
      <asp:Label runat="server" for="email_id">Email Id:</asp:Label>
       <asp:TextBox runat="server" class="form-control col-4" ID="email_id" name="emailid"></asp:TextBox>
      <asp:RegularExpressionValidator ID="RegularExpressionValidator1" runat="server" ErrorMessage="Enter Valid emal id " ControlToValidate="email_id" ValidationExpression="\w+([-+.']\w+)*@\w+([-.]\w+)*\.\w+([-.]\w+)*"></asp:RegularExpressionValidator>
 </div>
```

### 5. CustomValidator Control
- We can solve our purpose with ASP.NET validation control. But if you still don't find solution you can create your own custom validator control. 
 
- The custom validator allows the user to write a method to handle the validation of the value entered. It is used to compare the users input to a value in the database or the arithmetic validations for the controls.

### 6. ValidationSummary
- The ValidationSummary control is reporting control, which is used by the other validation controls on a page. 
 
- The validation summary control will collect all the error messages of all the non-valid controls and display them on the page.


# User Controls in ASP.NET
- An ASP.NET Web user control is similar to a complete ASP.NET Web page (.aspx file), with both a user interface page and code.
- The file name extension for the user control is .ascx.
- You create the user control in much the same way you create an ASP.NET page and then add the child controls that you need.
- User controls cannot run as stand-alone files. Instead, you must add them to ASP.NET pages.
- A UserControl also provides for reusability. In other words, we can create and edit in one thing and get results everywhere, wherever you use the item.
