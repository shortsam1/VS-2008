# VS-2008
Issue with Pop Up Boxes sometimes not working


Using ASP. Net 2008 with c# & PIUControls for a Risk Picker and Date Picker.
.net framework is 3.5.

Occasionaly on some pc's we have an issue where both of these pop up boxes do not work.  We are using Internet Explorer 11.

Most of the time one of the following things fixes the issue (Deleting the browsing history, Turning on the 'Compatibility View Settings', or Turning on 'Enterprise Mode')

However on the odd occasion this does not work.

The code for this is as follows:

<tr>

<td class="fieldLabel" >

<asp:label id="lblInitialRisk" runat="server"> Initial Risk Assessment</asp:label>

<a href="javascript:help_create('Current_Risk_Rating')"> <img  alt="" src="images/question_mark_icon.gif" border="0"  /> </a><br /> 

<asp:HyperLink id="link1"  runat="server"  Text="NSW Health Risk Matrix"  NavigateUrl="~/NSW_Health_Risk_Matrix_with_LHN_delegation.pdf" Target="_blank" />  <br />

<asp:RequiredFieldValidator ID="vldInitialRisk" ValidationGroup="Risk" runat="server"

ErrorMessage="Current Risk Rating must be entered" ControlToValidate="tbxInitialRisk" Font-Bold="True" Display="Dynamic" EnableClientScript="False">Current Risk Rating must be entered</asp:RequiredFieldValidator>

</td>

<td class="fieldValue" >

<PIUControlsX:RiskPicker ID="rpInitialRisk" runat="server" OnClick="tbxInitialRisk" EnableViewState="false" />

<asp:TextBox ID="tbxInitialRisk" CssClass ="hidden" runat="server" 

OnTextChanged="Priority_Changed" />

 <asp:label id="lblPriority" runat="server" >NSW Health Matrix Classification:  </asp:label>

<asp:label id="lblPriorityRating" runat="server" CssClass="readOnlyValue" Width="75px"></asp:label>

</td>

<td class="fieldValue">

<asp:TextBox ID="tbxCurrentRisk" CssClass="hidden" runat="server"></asp:TextBox>

</td>

 <td class="fieldValue">

<asp:label id="lblPriorityRating_R" runat="server" CssClass="readOnlyValue" Width="75px" Visible="false"></asp:label>

</td>

</tr>

<tr>

<td class="fieldLabel" >

<asp:label id="lblInitialDate" runat="server">Date Risk Created</asp:label>

<a href="javascript:help_create('Current_risk_rating_date')"> <img  alt="" src="images/question_mark_icon.gif" border="0"  /> </a><br />

<asp:RequiredFieldValidator ID="vldInitialDate" runat="server" ControlToValidate="tbxInitialDate" ValidationGroup="Risk"

ErrorMessage="Current Risk Rating Date must be entered" Display="Dynamic" Font-Bold="True">

Current risk rating date must be entered</asp:RequiredFieldValidator>

</td>

<td valign="middle" >

<PIUControls:datepicker id="dpInitialDate" runat="server" DateType="d mmm yyyy" EnableViewState="false"></PIUControls:datepicker>

<asp:TextBox ID="tbxInitialDate" runat="server" Width="72px" CssClass="hidden" ></asp:TextBox>

</td>

</tr>


Both the PIUControls and PIUControlsX are .dll files. I am unure as how to share them.  I cannot find links to them.  They are under the references section in asp.net but I am unsure as to what library they are found in.

The files are referenced in the system at the beginning of the page.

<%@  Register assembly="PIUControlsX" namespace="PIUControlsX" tagprefix="PIUControlsX" %>

<%@  Register assembly="PIUControls" namespace="PIUControls" tagprefix="PIUControls" %>

I inherited this system and have been maintaining it.


I am new to this.

Any ideas??
