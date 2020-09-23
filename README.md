<div align="center">

## No Refresh, No NAV Back\*, No Right Click, No Backspace, etc\.


</div>

### Description

To disable the right click, the backspace (for navigation purposes), and the refresh.
 
### More Info
 
*Obviously for this script to run effectively you MUST open up a NEW browser window in IE using JScript. Please note that for this script to run effectively it is recommended that you open a new browser using script to disable the navigation, link bars, etc., etc. Also, the cool thing about this code is that the JavaScript disables itself once the cursor is in a text are box, or input box - VERY COOL! PLEASE NOTE, THIS CODE WAS ONLY TESTED IN IE 5.0+. If you feel you can add to this code to make it better, be my guest. Send me the updated code and I will paste it right here.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Matt Khoury](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/matt-khoury.md)
**Level**          |Advanced
**User Rating**    |4.5 (45 globes from 10 users)
**Compatibility**  |
**Category**       |[Browser/ System Services](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/browser-system-services__2-69.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/matt-khoury-no-refresh-no-nav-back-no-right-click-no-backspace-etc__2-2250/archive/master.zip)





### Source Code

```
<HTML>
<HEAD>
	<TITLE>NO REFRESH, NO REFRESH, NO BACKSPACE, NO ALT-BACKSPACE, ETC., ETC..</TITLE>
<SCRIPT LANGUAGE=JAVASCRIPT>
var oLastBtn=0;
	bIsMenu = false;
	//No RIGHT CLICK************************
	// ****************************
	if (window.Event)
	document.captureEvents(Event.MOUSEUP);
	function nocontextmenu()
	{
	event.cancelBubble = true
	event.returnValue = false;
	return false;
	}
	function norightclick(e)
	{
	if (window.Event)
	{
	if (e.which !=1)
	return false;
	}
	else
	if (event.button !=1)
	{
	event.cancelBubble = true
	event.returnValue = false;
	return false;
	}
	}
	document.oncontextmenu = nocontextmenu;
	document.onmousedown = norightclick;
	//**************************************
	// ****************************
	// Block backspace onKeyDown************
	// ***************************
	 function onKeyDown() {
	 	if ( (event.altKey) || ((event.keyCode == 8) &&
	 			(event.srcElement.type != "text" &&
	 			event.srcElement.type != "textarea" &&
	 			event.srcElement.type != "password")) ||
	 			((event.ctrlKey) && ((event.keyCode == 78) || (event.keyCode == 82)) ) ||
	 			(event.keyCode == 116) ) {
	 		event.keyCode = 0;
	 		event.returnValue = false;
	 	}
	 }
</SCRIPT>
</HEAD>
<BODY onKeyDown="onKeyDown();" BGCOLOR="#639ace" MARGINHEIGHT="0" MARGINWIDTH="0" TOPMARGIN="0" LEFTMARGIN="0">
<TABLE WIDTH="100%" BORDER="0" CELLSPACING="0" CELLPADDING="0">
	<TR>
		<TD><H3>NO REFRESH, NO REFRESH, NO BACKSPACE, NO ALT-BACKSPACE, ETC., ETC..</H3></TD>
	</TR>
	<TR>
		<TD>Please note that for this script to run effectively it is recommended that you open a new browser using script to disable the navigation, link bars, etc., etc..</TD>
	</TR>
</TABLE>
</BODY>
</HTML>
```

