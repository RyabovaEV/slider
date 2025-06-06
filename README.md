# 📸 Простой бесконечный слайдер изображений на JavaScript

Этот слайдер реализует автоматическую прокрутку изображений с плавной анимацией, бесконечной прокруткой (infinite loop) и поддержкой адаптивности.

## 🚀 Возможности
- Бесконечная прокрутка: слайды зациклены с помощью дубликатов первого и последнего элементов.
- Плавная анимация: используется CSS translate с переходом.
- Навигация: кнопки "вперёд" и "назад" переключают слайды.
- Адаптивность: позиционирование слайдов пересчитывается при изменении размера окна.

## 🧩 Использование

### HTML
``` 
<div class="slider-wrapper">
  <button data-btn-prev>←</button>
  <div class="slider" data-slider></div>
  <button data-btn-next>→</button>
</div>
```

### JavaScript
```
// Подключите JS-код слайдера (см. файл slider.js)
```

### Массив изображений
```
const images = [
  "https://placehold.co/800x400?text=Slice+1",
  "https://placehold.co/1800x400?text=Slice+2",
  "https://placehold.co/800x400?text=Slice+3",
  "https://placehold.co/800x400?text=Slice+4",
  "https://placehold.co/800x400?text=Slice+5",
];
```

## ⚙️ Как это работает

1. setupSlider() – добавляет изображения в DOM и создаёт дубликаты для бесконечной прокрутки.

2. initSlider() – устанавливает начальное смещение для правильного отображения.

3. goToPrevSlide() и goToNextSlide() – обрабатывают переходы между слайдами, обеспечивая плавную бесконечную анимацию.

4. Событие resize – пересчитывает ширину слайдов при изменении размера окна.


## 📝 Примечания

- Дубликаты первого и последнего слайдов позволяют добиться эффекта бесшовной анимации.

- Используется translate вместо left или margin, что обеспечивает лучшую производительность.

- Чтобы слайдер работал корректно, задайте фиксированную ширину изображениям через CSS или используйте одинаковые размеры изображений.
