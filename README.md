## Link maker

JS coming soon

<input id="url" placeholder="Enter url" />
<a id="link"  style="display: block; padding: 10; border: 1px solid;"> - GO - </a>

<script type="text/javascript">
let params = (new URL(location)).searchParams;
var input = document.getElementById('url')
var link = document.getElementById('link')
link.href = params.default
input.value = params.default
input.onchange = () => {
  link.href = input.value
}
</script>
