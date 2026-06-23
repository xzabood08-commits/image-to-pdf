# image-to-pdf
تحويل الصور إلى ملف PDF بسهولة أونلاين
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تحويل الصور إلى PDF احترافي</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
    <style>
        /* تنسيق الخلفية العامة للموقع */
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%); 
            min-height: 100vh;
            margin: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        
        /* تنسيق الصندوق الأبيض الأساسي */
        .container { 
            background: white; 
            padding: 40px 30px; 
            border-radius: 20px; 
            max-width: 450px; 
            width: 100%;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1); 
            text-align: center;
        }

        /* عنوان الأداة */
        h2 { 
            color: #2c3e50; 
            margin-bottom: 10px;
            font-size: 24px;
        }

        /* الوصف المساعد */
        p {
            color: #7f8c8d;
            font-size: 14px;
            margin-bottom: 30px;
        }

        /* تنسيق منطقة اختيار الصور */
        .file-drop-area {
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            padding: 25px;
            border: 2px dashed #3498db;
            border-radius: 12px;
            background-color: #f8fafc;
            transition: 0.3s;
            cursor: pointer;
            margin-bottom: 25px;
        }

        .file-drop-area:hover {
            background-color: #ebf5fb;
            border-color: #2980b9;
        }

        /* إخفاء زر الاختيار الافتراضي البشع وتكبير مساحة الضغط */
        input[type="file"] { 
            position: absolute;
            left: 0;
            top: 0;
            height: 100%;
            width: 100%;
            opacity: 0;
            cursor: pointer;
        }

        .file-msg {
            font-size: 15px;
            color: #34495e;
            font-weight: 500;
        }

        /* تنسيق زر التحويل المودرن */
        button { 
            background: linear-gradient(135deg, #2ecc71 0%, #27ae60 100%); 
            color: white; 
            border: none; 
            padding: 14px; 
            font-size: 16px; 
            font-weight: bold;
            border-radius: 10px; 
            cursor: pointer; 
            width: 100%; 
            box-shadow: 0 4px 15px rgba(46, 204, 113, 0.3);
            transition: transform 0.2s, box-shadow 0.2s; 
        }

        button:hover { 
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(46, 204, 113, 0.4);
        }

        button:active {
            transform: translateY(0);
        }
    </style>
</head>
<body>

<div class="container">
    <h2>تطبيق تحويل الصور إلى PDF</h2>
    <p>اضغط في الأسفل لاختيار صورك، ثم ارفعها دفعة واحدة</p>
    
    <div class="file-drop-area">
        <span class="file-msg" id="statusMsg">📁 اضغط هنا لاختيار الصور</span>
        <input type="file" id="imageInput" accept="image/*" multiple onchange="updateCount()">
    </div>
    
    <button onclick="convertToPDF()">توليد وتحميل ملف PDF</button>
</div>

<script>
    // تحديث النص ليظهر عدد الصور المحددة بشكل جميل
    function updateCount() {
        const input = document.getElementById('imageInput');
        const msg = document.getElementById('statusMsg');
        if (input.files.length > 0) {
            msg.innerHTML = `✅ تم اختيار (${input.files.length}) صور بنجاح`;
            msg.style.color = '#27ae60';
        } else {
            msg.innerHTML = `📁 اضغط هنا لاختيار الصور`;
            msg.style.color = '#34495e';
        }
    }

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
