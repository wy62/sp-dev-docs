---


manager: laurawi
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- SharePoint workflows
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cd9ce74a-ac5a-4ebc-8e4c-3b16bcad828e
---

![Collapse
section](../icons/collapse_all.gif "Collapse section")![Expand
section](../icons/expand_all.gif "Expand section")![](../icons/collapse_all.gif)![](../icons/expand_all.gif)![](../icons/dropdown.gif)![](../icons/dropdownHover.gif)![Copy
code](../icons/copycode.gif "Copy code")![Copy code
hover](../icons/copycodeHighlight.gif "Copy code hover")
<table>
<tbody>
<tr class="odd">
<td align="left"></td>
</tr>
</tbody>
</table>

Visual Basic  
C\#  
C++  
JavaScript  

<table>
<tbody>
<tr class="odd">
<td align="left"><span id="runningHeaderText"></span></td>
</tr>
<tr class="even">
<td align="left"># Action Element (WorkflowInfo)</td>
</tr>
<tr class="odd">
<td align="left"><a href="#exampleToggle">Example</a>  <a href="#seeAlsoToggle">See also</a>  <span id="headfeedbackarea" class="feedbackhead"><a href="javascript:SubmitFeedback(&#39;docthis@Microsoft.com&#39;,&#39;&#39;,&#39;&#39;,&#39;&#39;,&#39;1.0.18082.1225&#39;,&#39;%0\dThank%20you%20for%20your%20feedback.%20The%20developer%20writing%20teams%20use%20your%20feedback%20to%20improve%20documentation.%20While%20we%20are%20reviewing%20your%20feedback,%20we%20may%20send%20you%20e-mail%20to%20ask%20for%20clarification%20or%20feedback%20on%20a%20solution.%20We%20do%20not%20use%20your%20e-mail%20address%20for%20any%20other%20purpose%20and%20we%20delete%20it%20after%20we%20finish%20our%20review.%0\AFor%20further%20information%20about%20the%20privacy%20policies%20of%20Microsoft,%20please%20see%20http://privacy.microsoft.com/en-us/default.aspx.%0\A%0\d&#39;,&#39;Customer%20feedback&#39;);">Send feedback</a></span></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"></td>
</tr>
</tbody>
</table>

**Last modified:** March 09, 2015

***Applies to:** SharePoint 2016 | SharePoint Foundation 2013 |
SharePoint Online | SharePoint Server 2013*

Contains the information that is needed for the workflow engine to
process a workflow activity, which is called an <span
class="term">action</span> in Microsoft SharePoint Foundation 2010. A
workflow **Action** element represents a
workflow activity, such as sending email notifications, updating
SharePoint Foundation 2010 list items, creating and assigning tasks, and
many other activities.

By default, SharePoint Foundation 2010 provides 23 built-in workflow
actions. These are defined in the WSS.ACTIONS file.

<span codelanguage="other"></span>
<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><pre><code>&lt;Actions&gt;
    &lt;Action&gt;
        &lt;Parameters&gt;
        &lt;/Parameters&gt;
        &lt;RuleDesigner&gt;
        &lt;/RuleDesigner&gt;
        &lt;DataSources&gt;
        &lt;/DataSources&gt;
        &lt;Modifications&gt;
            &lt;Modification&gt;
            &lt;/Modification&gt;
        &lt;/Modifications&gt;
        &lt;ActionVariables&gt;
        &lt;/ActionVariables&gt;
        &lt;ActionBody&gt;
        &lt;/ActionBody&gt;
        &lt;ActionConditions&gt;
        &lt;/ActionConditions&gt;
    &lt;/Action&gt;
&lt;/Actions&gt;</code></pre></td>
</tr>
</tbody>
</table>


-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><p>Attribute</p></th>
<th align="left"><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>**Name**</p></td>
<td align="left"><p>Required **text**. Represents the description of the workflow action that is displayed to the workflow editor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>**ClassName**</p></td>
<td align="left"><p>Required **text</span>. Fully qualified name of the class that implements the workflow action; for example, <span sdata="cer" target="T:Microsoft.SharePoint.WorkflowActions.EmailActivity"><span class="nolink">Microsoft.SharePoint.WorkflowActions.EmailActivity</span>**.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>**Assembly**</p></td>
<td align="left"><p>Required **text</span>. The Microsoft .NET assembly name that contains instructions to implement the <span class="keyword">Action** element. The text should include the PublicKeyToken, Version, and Culture.</p></td>
</tr>
<tr class="even">
<td align="left"><p>**FunctionName**</p></td>
<td align="left"><p>Optional **text**. For sandboxed solutions, specifies the name of a function to call.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>**Category**</p></td>
<td align="left"><p>Optional **text</span>. Provides a category for the workflow action. This <span class="keyword">text** is used to filter the list of available actions.</p></td>
</tr>
<tr class="even">
<td align="left"><p>**CreatesTask**</p></td>
<td align="left"><p>Optional **Boolean</span>. If set to <span class="keyword">true</span>, a task list item is created in the workflow. If left blank, the assumption is <span class="keyword">false**, and no task list items are created.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>**CreatesInList**</p></td>
<td align="left"><p>Optional **text</span>. If a value is set for this attribute, the workflow creates an item in a list. Values must map to a parameter name that contains the <span class="keyword">ID** of the list or document library.</p></td>
</tr>
<tr class="even">
<td align="left"><p>**AppliesTo**</p></td>
<td align="left"><p>Required **text</span>. Indicates whether this workflow action should be available for lists, document libraries, or both. Valid values include <span class="keyword">list</span>, <span class="keyword">doclib</span>, and <span class="keyword">all**.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>**IsError**</p></td>
<td align="left"><p>Optional **Boolean</span>. If set to <span class="keyword">true</span>, instances of this <span class="keyword">Action** element are considered an error by the client application.</p></td>
</tr>
<tr class="even">
<td align="left"><p>**ListModeration**</p></td>
<td align="left"><p>Optional **Boolean</span>. If set to <span class="keyword">true</span>, this <span class="keyword">Action</span> element applies to a list or document library that has content approval enabled. If left blank, the assumption is <span class="keyword">false**.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>**UsesCurrentItem**</p></td>
<td align="left"><p>Optional **Boolean</span>. If set to <span class="keyword">true</span>, indicates that the current item should be used or modified. If set to <span class="keyword">false</span> or left blank, this <span class="keyword">Action** element uses only the SharePoint list or document library item that is specified.</p></td>
</tr>
<tr class="even">
<td align="left"><p>**CreatedTaskFormType**</p></td>
<td align="left"><p>Optional **text</span>. Specifies the type of a created task: <span class="keyword">DataCollectTask</span> to create a task that collects data from one user; <span class="keyword">GroupAssignedTask</span> to create a task that collects data from one or more users; <span class="keyword">TodoItemTask</span> to create a task that does not collect data from users but only exists for a user to validate that they have done something; or <span class="keyword">TaskProcess** to create a task that has a form that allows for ad-hoc collaboration and might collect data from one or more users.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>**__SolutionId**</p></td>
<td align="left"><p>Optional **text**. Specifies a GUID that the client application writes to the implementation-specific action. The server uses the GUID to help locate the assembly at run time of the workflow.</p></td>
</tr>
<tr class="even">
<td align="left"><p>**SandboxedFunction**</p></td>
<td align="left"><p>Optional **Boolean</span>. If set to <span class="keyword">true</span>, the client application inserts an implementation-specific action when this action is selected. The action should be configured to call a function defined by the conjunction of <span class="keyword">AssemblyName</span>, <span class="keyword">ClassName</span>, and <span class="keyword">FunctionName</span>. If set, <span class="keyword">AssemblyName</span>, <span class="keyword">ClassName</span>, <span class="keyword">FunctionName</span>, and <span class="keyword">__SolutionId** must also be set.</p></td>
</tr>
</tbody>
</table>


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="parameters-element-workflowinfo.htm">Parameters</a></p>
<p><a href="ruledesigner-element-workflowinfo.htm">RuleDesigner</a></p>
<p><a href="datasources-element-workflowinfo.htm">DataSources</a></p>
<p><a href="modifications-element-workflowinfo.htm">Modifications</a></p>
<p><a href="actionvariables-element-workflowinfo.htm">ActionVariables</a></p>
<p><a href="actionbody-element-workflowinfo.htm">ActionBody</a></p>
<p><a href="actionconditions-element-workflowinfo.htm">ActionConditions</a></p></td>
</tr>
</tbody>
</table>


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="actions-element-workflowinfo.htm">Actions</a></p></td>
</tr>
</tbody>
</table>


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The following code example demonstrates how to construct an <span
class="keyword">Action</span> element so that it is displayed in the
workflow editor. Note that this XML has been modified for readability.

<span codelanguage="xmlLang"></span>
XML 
<span class="copyCode" onclick="CopyCode(this)"
onkeypress="CopyCode_CheckKey(this, event)"
onmouseover="ChangeCopyCodeIcon(this)"
onmouseout="ChangeCopyCodeIcon(this)" tabindex="0">![Copy
code](../icons/copycode.gif "Copy code")Copy code</span>
    <WorkflowInfo>
      <Conditions>…</Conditions>
      <Actions Sequential="then" Parallel="and">
        <Action Name="Update my custom SharePoint list"
                ClassName="CustomActivities.OrderListFunctions"
                Assembly="CustomActivities,      
                          PublicKeyToken=b03f5f7f11d50a3a, 
                          Version=1.0.0.0, 
                          Culture=neutral"
                Category="My Custom Actions"
                CreatesTask="true"
                CreatesInList="UpdateList"
                AppliesTo="all"
                ListModeration="false"
                UsesCurrentItem="true">
          <RuleDesigner Sentence="Update %1">
            <FieldBind Field="UpdateList"
                       Function="UpdateOrderList"
                       DesignerType="ChooseListItem"
                       ID="1"
                       Text="My Custom List">
            </FieldBind>
          </RuleDesigner>
          <Parameters>
            <Parameter Type="System.String, mscorlib"
                       Direction="In"
                       Name="UpdateList"
            </Parameters>
        </Action>
      </Actions>
    </WorkflowInfo>


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Tasks

[.ACTIONS File Example](actions-file-example-workflowinfo.htm)

#### Concepts

[Default Workflow Actions](default-workflow-actions-workflowinfo.htm)

[Default Workflow Conditions](default-workflow-conditions-workflowinfo.htm)

#### Other resources

[Creating Declarative, No-Code Workflow
Editors](http://msdn.microsoft.com/library/60dfda8d-e724-4d7d-9578-aa239c362dcf(Office.15).aspx)

[Workflow Actions Schema
Overview](http://msdn.microsoft.com/library/25da07cb-b228-43f2-9cdf-c8c71c3eabbb(Office.15).aspx)








