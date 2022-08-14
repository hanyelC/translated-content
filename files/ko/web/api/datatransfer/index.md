---
title: DataTransfer
slug: Web/API/DataTransfer
tags:
  - API
  - DataTransfer
  - HTML Drag and Drop API
  - Interface
  - Reference
  - Web Development
  - drag and drop
translation_of: Web/API/DataTransfer
---
<div>{{APIRef("HTML Drag and Drop API")}}</div>

<p>The <code><strong>DataTransfer</strong></code> object is used to hold the data that is being dragged during a drag and drop operation. It may hold one or more data items, each of one or more data types. For more information about drag and drop, see <a href="/en-US/docs/Web/API/HTML_Drag_and_Drop_API">HTML Drag and Drop API</a>.</p>

<p>This object is available from the {{domxref("DragEvent.dataTransfer","dataTransfer")}} property of all {{domxref("DragEvent","drag events")}}.</p>

<h2 id="Constructor">Constructor</h2>

<dl>
 <dt>{{domxref("DataTransfer.DataTransfer","DataTransfer()")}}</dt>
 <dd>Creates and returns a new <code>DataTransfer</code> object.</dd>
</dl>

<h2 id="Properties">Properties</h2>

<h3 id="Standard_properties">Standard properties</h3>

<dl>
 <dt>{{domxref("DataTransfer.dropEffect")}}</dt>
 <dd>Gets the type of drag-and-drop operation currently selected or sets the operation to a new type. The value must be <code>none</code>, <code>copy</code>, <code>link</code> or <code>move</code>.</dd>
 <dt>{{domxref("DataTransfer.effectAllowed")}}</dt>
 <dd>Provides all of the types of operations that are possible. Must be one of <code>none</code>, <code>copy</code>, <code>copyLink</code>, <code>copyMove</code>, <code>link</code>, <code>linkMove</code>, <code>move</code>, <code>all</code> or <code>uninitialized</code>.</dd>
 <dt>{{domxref("DataTransfer.files")}}</dt>
 <dd>Contains a list of all the local files available on the data transfer. If the drag operation doesn't involve dragging files, this property is an empty list.</dd>
 <dt>{{domxref("DataTransfer.items")}} {{readonlyInline}}</dt>
 <dd>Gives a {{domxref("DataTransferItemList")}} object which is a list of all of the drag data.</dd>
 <dt>{{domxref("DataTransfer.types")}} {{readonlyInline}}</dt>
 <dd>An array of {{domxref("DOMString","strings")}} giving the formats that were set in the {{event("dragstart")}} event.</dd>
</dl>

<h3 id="Gecko_properties">Gecko properties</h3>

<p>{{SeeCompatTable}}</p>

<div class="note"><strong>Note:</strong> All of the properties in this section are Gecko-specific.</div>

<dl>
 <dt>{{domxref("DataTransfer.mozCursor")}}</dt>
 <dd>Gives the drag cursor's state. This is primarily used to control the cursor during tab drags.</dd>
 <dt>{{domxref("DataTransfer.mozItemCount")}} {{readonlyInline}}</dt>
 <dd>Gives the number of items in the drag operation.</dd>
 <dt>{{domxref("DataTransfer.mozSourceNode")}} {{readonlyInline}}</dt>
 <dd>The {{ domxref("Node") }} over which the mouse cursor was located when the button was pressed to initiate the drag operation. This value is <code>null</code> for external drags or if the caller can't access the node.</dd>
 <dt>{{domxref("DataTransfer.mozUserCancelled")}} {{readonlyInline}}</dt>
 <dd>This property applies only to the <code>dragend</code> event, and is <code>true</code> if the user canceled the drag operation by pressing escape. It will be <code>false</code> in all other cases, including if the drag failed for any other reason, for instance due to a drop over an invalid location.</dd>
</dl>

<h2 id="Methods">Methods</h2>

<h3 id="Standard_methods">Standard methods</h3>

<dl>
 <dt>{{domxref("DataTransfer.clearData()")}}</dt>
 <dd>Remove the data associated with a given type. The type argument is optional. If the type is empty or not specified, the data associated with all types is removed. If data for the specified type does not exist, or the data transfer contains no data, this method will have no effect.</dd>
 <dt>{{domxref("DataTransfer.getData()")}}</dt>
 <dd>Retrieves the data for a given type, or an empty string if data for that type does not exist or the data transfer contains no data.</dd>
 <dt>{{domxref("DataTransfer.setData()")}}</dt>
 <dd>Set the data for a given type. If data for the type does not exist, it is added at the end, such that the last item in the types list will be the new format. If data for the type already exists, the existing data is replaced in the same position.</dd>
 <dt>{{domxref("DataTransfer.setDragImage()")}}</dt>
 <dd>Set the image to be used for dragging if a custom one is desired.</dd>
</dl>

<h3 id="Gecko_methods">Gecko methods</h3>

<p>{{Non-standard_header()}}</p>

<div class="note"><strong>Note:</strong> All of the methods in this section are Gecko-specific.</div>

<dl>
 <dt>{{domxref("DataTransfer.addElement()")}}</dt>
 <dd>Sets the drag source to the given element.</dd>
 <dt>{{domxref("DataTransfer.mozClearDataAt()")}}</dt>
 <dd>Removes the data associated with the given format for an item at the specified index. The index is in the range from zero to the number of items minus one.</dd>
 <dt>{{domxref("DataTransfer.mozGetDataAt()")}}</dt>
 <dd>Retrieves the data associated with the given format for an item at the specified index, or null if it does not exist. The index should be in the range from zero to the number of items minus one.</dd>
 <dt>{{domxref("DataTransfer.mozSetDataAt()")}}</dt>
 <dd>A data transfer may store multiple items, each at a given zero-based index. <code>mozSetDataAt()</code> may only be called with an index argument less than <code>mozItemCount</code> in which case an existing item is modified, or equal to <code>mozItemCount</code> in which case a new item is added, and the <code>mozItemCount</code> is incremented by one.</dd>
 <dt>{{domxref("DataTransfer.mozTypesAt()")}}</dt>
 <dd>Holds a list of the format types of the data that is stored for an item at the specified index. If the index is not in the range from 0 to the number of items minus one, an empty string list is returned.</dd>
</dl>

<h2 id="Example">Example</h2>

<p>Every method and property listed in this document has its own reference page and each reference page either directly includes an example of the interface or has a link to an example.</p>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>



<p>{{Compat("api.DataTransfer")}}</p>

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/HTML_Drag_and_Drop_API">Drag and drop</a></li>
 <li><a href="/en-US/docs/Web/Guide/HTML/Drag_operations">Drag Operations</a></li>
 <li><a href="/en-US/docs/Web/Guide/HTML/Recommended_Drag_Types">Recommended Drag Types</a></li>
 <li><a href="/en-US/docs/Web/Guide/HTML/Dragging_and_Dropping_Multiple_Items">Dragging and Dropping Multiple Items</a></li>
 <li><a href="https://codepen.io/tech_query/pen/MqGgap">DataTransfer test - Paste or Drag</a></li>
</ul>