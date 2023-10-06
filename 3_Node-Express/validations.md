```js
// Валидация файлов
            if (!req.files) { // req.files -> null
            return res.status(400).send('No files were uploaded.');
            }

// валидация данных
        if (!req.body) {
            return res.status(400).send('No request body found');
        }