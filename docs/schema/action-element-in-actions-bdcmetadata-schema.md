---
ms.author: NormSohl
author: NormSohl
manager: soliver
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- VS.SharePointTools.BDC.Action Element
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f58b96c0-77a8-69d3-8710-fff03d4970b9
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
<td align="left"># Action Element in Actions (BDCMetadata Schema)</td>
</tr>
<tr class="odd">
<td align="left"><span id="headfeedbackarea" class="feedbackhead"><a href="javascript:SubmitFeedback(&#39;docthis@Microsoft.com&#39;,&#39;&#39;,&#39;&#39;,&#39;&#39;,&#39;1.0.18082.1225&#39;,&#39;%0\dThank%20you%20for%20your%20feedback.%20The%20developer%20writing%20teams%20use%20your%20feedback%20to%20improve%20documentation.%20While%20we%20are%20reviewing%20your%20feedback,%20we%20may%20send%20you%20e-mail%20to%20ask%20for%20clarification%20or%20feedback%20on%20a%20solution.%20We%20do%20not%20use%20your%20e-mail%20address%20for%20any%20other%20purpose%20and%20we%20delete%20it%20after%20we%20finish%20our%20review.%0\AFor%20further%20information%20about%20the%20privacy%20policies%20of%20Microsoft,%20please%20see%20http://privacy.microsoft.com/en-us/default.aspx.%0\A%0\d&#39;,&#39;Customer%20feedback&#39;);">Send feedback</a></span></td>
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

Specifies an action supported by an external content type.

**Namespace:**
http://schemas.microsoft.com/windows/2007/BusinessDataCatalog

**Schema:** BDCMetadata

Actions bridge the gap between Microsoft SharePoint 2010 and Microsoft
Office 2010 and an external system's user interface by providing a link
back to the external system.

By default, Business Data Connectivity (BDC) service provides actions
such as **View Item**, <span
class="keyword">Edit Item</span>, and <span class="keyword">Delete
Item</span> after you model these operations in the BDC model. In
addition to these default actions, you can create actions for other
functionality you want to attach to your external content type. For
example, you can use actions to perform simple actions such as to send
e-mail messages to a customer from the Customer external content type or
to open a customer's home page in a browser.

Actions travel with an external content type. That is, after you define
an action for an external content type, the action appears everywhere
you display that external content type—whether in an external list or
Business Data Web Part or in an External Data column.

<span codelanguage="xmlLang"></span>
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><pre><code>&lt;Action Position = &quot;Integer&quot; IsOpenedInNewWindow = &quot;Boolean&quot; Url = &quot;String&quot; ImageUrl = &quot;String&quot; Name = &quot;String&quot; DefaultDisplayName = &quot;String&quot; IsCached = &quot;Boolean&quot;&gt; &lt;/Action&gt;</code></pre></td>
</tr>
</tbody>
</table>


--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The following sections describe attributes, child elements, and parent
elements.

#### Attributes

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
<td align="left"><p>**Position**</p></td>
<td align="left"><p>Required.</p>
<p>The suggested position of this action among the other actions of this external content type.</p>
<p>Attribute type: **Integer**</p></td>
</tr>
<tr class="even">
<td align="left"><p>**IsOpenedInNewWindow**</p></td>
<td align="left"><p>Optional.</p>
<p>Specifies whether the results of executing an action are presented in a new user interface window.</p>
<p>Default value: **false**</p>
<p>Attribute type: **Boolean**</p></td>
</tr>
<tr class="odd">
<td align="left"><p>**Url**</p></td>
<td align="left"><p>Required.</p>
<p>The URL to go to when the action is invoked. The URL string is a Microsoft .NET Framework format string. Each format specifier (for example, {0}) corresponds to an **Action** parameter.</p>
<p>Attribute type: **String**</p></td>
</tr>
<tr class="even">
<td align="left"><p>**ImageUrl**</p></td>
<td align="left"><p>Optional.</p>
<p>The absolute or relative path to the icon image for the action. The icon image should be 16 x 16 pixels.</p>
<p>Attribute type: **String**</p></td>
</tr>
<tr class="odd">
<td align="left"><p>****Name</p></td>
<td align="left"><p>Required.</p>
<p>The name of this action.</p>
<p>Attribute type: **String**</p></td>
</tr>
<tr class="even">
<td align="left"><p>**DefaultDisplayName**</p></td>
<td align="left"><p>Optional.</p>
<p>The default display name for this action.</p>
<p>Attribute type: **String**</p></td>
</tr>
<tr class="odd">
<td align="left"><p>**IsCached**</p></td>
<td align="left"><p>Optional.</p>
<p>Specifies whether this action is used frequently. This is used by the BDC client runtime to cache this action.</p>
<p>Default value: **true**</p>
<p>Attribute type: **Boolean**</p></td>
</tr>
</tbody>
</table>

#### Child elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><p>Element</p></th>
<th align="left"><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span sdata="link"><a href="localizeddisplaynames-element-in-metadataobject-bdcmetadata-schema.htm">LocalizedDisplayNames Element in MetadataObject (BDCMetadata Schema)</a></span></p></td>
<td align="left"><p>The localized names of the action.</p></td>
</tr>
<tr class="even">
<td align="left"><p><span sdata="link"><a href="properties-element-in-metadataobject-bdcmetadata-schema.htm">Properties Element in MetadataObject (BDCMetadata Schema)</a></span></p></td>
<td align="left"><p>The properties of the action.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><span sdata="link"><a href="actionparameters-element-in-action-bdcmetadata-schema.htm">ActionParameters Element in Action (BDCMetadata Schema)</a></span></p></td>
<td align="left"><p>The parameters of the action.</p></td>
</tr>
</tbody>
</table>

#### Parent elements

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><p>Element</p></th>
<th align="left"><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span sdata="link"><a href="actions-element-in-entity-bdcmetadata-schema.htm">Actions Element in Entity (BDCMetadata Schema)</a></span></p></td>
<td align="left"><p>The list of actions of an external content type.</p></td>
</tr>
</tbody>
</table>

![Footer](../icons/footer.gif "Footer")

[© 2013 Microsoft Corporation. All rights
reserved.](office-2013-documentation-copyright-notice.htm)



