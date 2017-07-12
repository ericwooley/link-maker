## Link maker

JS coming soon

<input id="url" placeholder="Enter url" />
<a id="link"> - GO - </a>

<script type="text/javascript">

var input = document.getElementById('url')
var link = document.getElementById('link')
input.onchange = () => link.href = input.value

</script>
