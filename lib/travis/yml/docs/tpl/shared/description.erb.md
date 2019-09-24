# <%= title_with_key %>

<% if summary %>
*<%= summary %>*
<% end %>

<%= description %>

<% if flags.include?(:expand) %>
The key `<%= id %>` is a [matrix expand key](/v1/docs/matrix_expand_keys), creating one or more additional jobs in your build matrix, depending how many other matrix expand keys are used.
<% end %>

<% if flags.include?(:edge) %>
The key `<%= id %>` is experimental and potentially might change or be removed.
<% end %>

<% if prefix %>
This node uses the key `<%= prefix[:key] %>` as a [default prefix](<%= path_to('types#map') %>) if not given a [map](<%= path_to('types') %>).
<% end %>

<%= render 'shared/deprecated' %>
<%= render 'shared/see' %>
<%#= render 'shared/known_on' %>