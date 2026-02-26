<div id="readme-content" style="padding: 20px; max-width: 800px; margin: auto; background: white; color: black; border-radius: 10px;">
    Loading portfolio details...
</div>

<script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>

<script>
    // جلب ملف README.md وعرضه
    fetch('README.md')
        .then(response => response.text())
        .then(text => {
            document.getElementById('readme-content').innerHTML = marked.parse(text);
        })
        .catch(err => {
            console.error('Error loading README:', err);
            document.getElementById('readme-content').innerHTML = "Could not load content.";
        });
</script>
