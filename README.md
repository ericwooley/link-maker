## Link maker
Enter in a link that you can click, for easy testing of android intents, but maybe you would like to use it for something else?

[Open here](https://ericwooley.github.io/link-maker)<br />

-- Ignore the stuff below this

<input id="url" placeholder="Enter url" style="display: block; padding: 10px 0 10px 0; width: 100%" />
<a id="link" target="_blank" style="display: block; padding: 10; border: 1px solid; text-align: center; minHeight: 100px; margin: 20px;"> - GO - </a>
<a id="permalink" target="_blank" style="display: block; padding: 10; border: 1px solid; text-align: center;" href=""></a>
<script type="text/javascript">
var getParam = location.href.split('?default=')[1]
var input = document.getElementById('url')
var link = document.getElementById('link')
var permaLink = document.getElementById('permalink')
link.href = decodeURIComponent(getParam)
input.value = decodeURIComponent(getParam)
function setPermalinkValue () {
  var val = window.location.origin + window.location.pathname + '?default=' + encodeURIComponent(input.value);
  permalink.href = val;
  permalink.innerHTML = val;
}
setPermalinkValue()
input.onchange = function () {
  link.href = input.value
  setPermalinkValue()
}
</script>
