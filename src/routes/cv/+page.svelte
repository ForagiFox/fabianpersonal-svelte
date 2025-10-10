<script>
  import PdfViewer from 'svelte-pdf';
let showButtons = ['zoom', 'rotate'];
</script>

<PdfViewer url="CV_ATS.pdf" {showButtons} />
