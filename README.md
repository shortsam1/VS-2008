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
