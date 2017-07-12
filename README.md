## Link maker

JS coming soon

<input id="url" placeholder="Enter url" />
<a id="link"> - GO - </a>

<script type="text/javascript" style="display: block; padding: 10; border: 1px solid;">

var input = document.getElementById('url')
var link = document.getElementById('link')
input.onchange = () => link.href = input.value

</script>
