## Link maker

JS coming soon

<input id="url" placeholder="Enter url" />
<a id="link" style="display: block; padding: 10; border: 1px solid; text-align: ceter;"> - GO - </a>
<a id="permalink" style="display: block; padding: 10; border: 1px solid; text-align: ceter;"></a>
<script type="text/javascript">
let params = (new URL(location)).searchParams;
var input = document.getElementById('url')
var link = document.getElementById('link')
var permaLink = document.getElementById('permalink')
link.href = params.get('default')
input.value = params.get('default')

function setPermalinkValue () {
  var val = window.location.origin + window.location.pathname + '?default=' + encodeURIComponent(input.value)
  permalink.href = val
  permalink.innerHTML = val
}

input.onchange = () => {
  link.href = input.value
  setPermalinkValue()
}
</script>
