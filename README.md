# Positivus

https://alekseevb.github.io/positivus/

Сайт "Positivus" сверстан по макету из фигмы, во время проекта я использовал:

- Препроцессор sass на диалекте scss
- Современные html теги dialog, time, summary, address, details
- Разметку по БЭМ методологии
- Подход к проектированию mobile first и desktop first

## Теги

`dialog` - был использован для модального окна бургер меню

`time` - был использован для обозначения времени в тексте, для того чтобы поисковые машины видели дату и время

`address` - был использован для обозначения контактной информации о компании 

*Тег `<address>` обрабатывается браузерами с использованием особых стилей, таких как курсива, что помогает выделить его в тексте и делает более очевидным для пользователей, что информация в этом элементе относится к контактным данным. Это также улучшает доступность, так как специализированные программы для чтения с экрана могут интерпретировать и правильно озвучивать адресную информацию.* 

`details` - использовался для создания раскрывающегося блока (для полной реализации этого блока также был использован тег `summary`) 
![[Pasted image 20250219122513.png]]

## Пример

```scss
@mixin fluid-text($max: 48, $min: 16) {
  font-size: clamp(#{$min}px, #{$max / 1440 * 100}vw, #{$max}px);
}

@mixin reset-link {
  color: inherit;

  &,
  &:hover {
    text-decoration: none;
  }
}

@mixin reset-button {
  padding: 0;
  background-color: transparent;
  border: none;
}

@mixin flex-center($isInline: false) {
  @if $isInline {
    display: inline-flex;
  } @else {
    display: flex;
  }

  justify-content: center;
  align-items: center;
}

@mixin abs-center {
  position: absolute;
  top: 50%;
  left: 50%;
  translate: -50% -50%;
}

@mixin square($size) {
  width: $size;
  aspect-ratio: 1;
}

@mixin visually-hidden {
  position: absolute !important;
  width: 1px !important;
  height: 1px !important;
  margin: -1px !important;
  border: 0 !important;
  padding: 0 !important;
  white-space: nowrap !important;
  clip-path: inset(100%) !important;
  clip: rect(0 0 0 0) !important;
  overflow: hidden !important;
}
```

