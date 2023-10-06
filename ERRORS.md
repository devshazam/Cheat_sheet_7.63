STATUS: подсчет всех ошибок и выявление новых


EXTRIM ERRORS CLIENT (sistem crash)==================================
    - property of undefined
        - Фильтровать нужно только результаты промисов







ERRORS CLIENT =======================================================
- Сложение чисел в javascript дают не предсказуемые результаты из-за динамической типизации (87114.15 + 20844.76 = 107958.90999999999) 
        - РЕШЕНИЕ: округление 
- The build failed because the process exited too early. This probably means the system ran out of memory or someone called
        - https://www.digitalocean.com/community/tutorials/how-to-add-swap-space-on-ubuntu-18-04







ERRORS SERVER =======================================================
- return res.status(201).json({message: "Заказ не найден!"}); - если status(201) содержит код ошибки не 400 и не 500 он не сработает!