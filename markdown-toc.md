var result = toc('# AAA\n## BBB\n### CCC\nfoo');
var str = '';

result.json.forEach(function(heading) {
  str += toc.linkify(heading.content);
});