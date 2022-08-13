---
title: Document.head
slug: Web/API/Document/head
translation_of: Web/API/Document/head
---
<p>{{APIRef("DOM")}}</p>

<p>Devuelve el elemento {{HTMLElement("head")}} del documento actual. Si hay más de un elemento <code>&lt;head&gt;</code>, devuelve el primero de estos.</p>

<h2 id="Syntax" name="Syntax">Sintaxis</h2>

<pre class="syntaxbox"><em>var objRef</em> = document.head;
</pre>

<h2 id="Example" name="Example">Ejemplo</h2>

<pre class="brush: js">// en el HTML: &lt;head id="my-document-head"&gt;
var aHead = document.head;

alert(aHead.id); // "my-document-head";

alert( document.head === document.querySelector("head") ); // true
</pre>

<h2 id="Example" name="Example">Notas</h2>

<p><code>document.head</code> is de sólo lectura. Cualquier intento de asignar un valor a esta propiedad fallará silenciosamente o, en caso de que se encuentre en <a href="/en-US/docs/Web/JavaScript/Reference/Functions_and_function_scope/Strict_mode">Modo estricto de ECMAScript</a> en un navegador Gecko, lanzará un <a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypeError"><code>TypeError</code></a>.</p>

<h2 id="Browser_Compatibility" name="Browser_Compatibility" style="line-height: 30px; font-size: 2.14285714285714rem;">Compatibilidad con navegadores</h2>

{{Compat("api.Document.head")}}

<h2 id="Specification" name="Specification">Especificación</h2>

<ul>
 <li><a href="http://www.w3.org/TR/html5/dom.html#dom-tree-accessors">HTML5: DOM Tree Accessors</a></li>
</ul>