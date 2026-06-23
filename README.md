# image-to-pdf
تحويل الصور إلى ملف PDF بسهولة أونلاين
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تحويل الصور إلى PDF</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <style>
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; text-align: center; background: #f4f7f6; padding: 40px 20px; color: #333; }
        .container { background: white; padding: 30px; border-radius: 15px; max-width: 500px; margin: auto; box-shadow: 0 4px 15px rgba(0,0,0,0.1); }
        h2 { color: #007bff; }
        input[type="file"] { margin: 20px 0; display: block; width: 100%; box-sizing: border-box; padding: 10px; background: #e9ecef; border-radius: 5px; }
        button { background: #28a745; color: white; border: none; padding: 12px 25px; font-size: 16px; border-radius: 5px; cursor: pointer; width: 100%; transition: 0.3s; }
        button:hover { background: #218838; }
    </style>
</head>
<body>

<div class="container">
    <h2>أداة تحويل الصور إلى PDF</h2>
    <p>اختر الصور من جهازك ثم اضغط على زر التحويل والتحميل</p>
    <input type="file" id="imageInput" accept="image/*" multiple>
    <button onclick="convertToPDF()">تحويل وتحميل PDF الآن</button>
</div>

<script>
    async function convertToPDF() {
        const { jsPDF } = window.jspdf;
        const input = document.getElementById('imageInput');
        
        if (input.files.length === 0) {
            alert('الرجاء اختيار صورة واحدة على الأقل!');
            return;
        }

        const doc = new jsPDF();
        
        for (let i = 0; i < input.files.length; i++) {
            const file = input.files[i];
            const imageData = await readFileAsDataURL(file);
            
            if (i > 0) doc.addPage();
            doc.addImage(imageData, 'JPEG', 10, 10, 190, 277); 
        }
        
        doc.save('images-converted.pdf');
    }

    function readFileAsDataURL(file) {
        return new Promise((resolve) => {
            const reader = new FileReader();
            reader.onload = (event) => resolve(event.target.result);
            reader.readAsDataURL(file);
        });
    }
</script>

</body>
</html>
