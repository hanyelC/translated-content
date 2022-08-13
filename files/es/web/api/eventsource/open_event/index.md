---
title: EventSource.onopen
slug: Web/API/EventSource/open_event
translation_of: Web/API/EventSource/onopen
original_slug: Web/API/EventSource/onopen
---
<div>{{APIRef('WebSockets API')}}</div>

<p>La propiedad <code><strong>onopen</strong></code> de la interfaz  {{domxref("EventSource")}}  es un {{event("Event_handlers", "event handler")}} llamado cuando un evento  {{event("open")}} es recibido, esto pasa cuando la conexión fue solo abierta.</p>

<h2 id="Syntax">Syntax</h2>

<pre class="syntaxbox">eventSource.onopen = function</pre>

<h2 id="Ejemplos">Ejemplos</h2>

<pre class="brush: js">evtSource.onopen = function() {
  console.log("Connection to server opened.");
};</pre>

<div class="note">
<p><strong>Nota</strong>: Tu puedes encontrar un ejemplo completo en GitHub — ve <a href="https://github.com/mdn/dom-examples/tree/master/server-sent-events">Simple SSE demo using PHP.</a></p>
</div>

<h2 id="Especificaciones">Especificaciones</h2>

<table class="standard-table">
 <tbody>
  <tr>
   <th scope="col">Especificación</th>
   <th scope="col">Estado</th>
   <th scope="col">Comentario</th>
  </tr>
  <tr>
   <td>{{SpecName('HTML WHATWG', "comms.html#handler-eventsource-onopen", "onopen")}}</td>
   <td>{{Spec2('HTML WHATWG')}}</td>
   <td>Initial definition</td>
  </tr>
 </tbody>
</table>

<ul>
</ul>

<h2 id="Compatibilidad_con_navegadores">Compatibilidad con navegadores</h2>

{{Compat("api.EventSource.onopen")}}

<h2 id="Mira_también">Mira también</h2>

<ul>
 <li>{{domxref("EventSource")}}</li>
</ul>