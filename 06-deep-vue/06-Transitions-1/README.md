# Transitions-1

👶🏻 _Несложная задача_<br>
⭐ _Дополнительная задача_

На странице со списком митапов мы добавляли анимацию элементам списка митапов, а также смене состояния (список/календарь) через стандартные компоненты `transition` и `transition-group`.

Хотя шаблон усложнился не значительно, CSS на странице вырос. Есть два подхода. 

Первый - подключить стили с классами анимаций глобально и использовать их по имени. 

Второй - можно создать отдельные компоненты, чтобы использовать их всегда, когда нужны такие анимации. Для простых анимаций второй подход не даёт больших преимуществ, но является отличным решением, когда анимация сложная и требует описания её логики в JS с использованием [хуков анимации](https://vuejs.org/v2/guide/transitions.html#JavaScript-Hooks).

Требуется создать два небольших компонента:
- `FadeTransition` для `transition` с переключением содержимого через плавную прозрачность;
- `FadeTransitionGroup` для `transition-group` для списков с плавным движением и плавной прозрачностью.

Оба компонента:
- Не имеют входных параметров;
- Имеют слот по умолчанию;
- Реализуют `TransparentWrapper` обёртку над стандартными компонентами, в частности, должны работать их параметры (например, `tag`) и события без модификатора `native`.

*Примечание:* `scoped` стили на `FadeTransitionGroup` не сработают, так как требуется переопределить стили на верхних элементах, переданных в слот. Мы вернёмся к этой проблеме позже в другой задаче.

<img src="https://i.imgur.com/V2AHP5H.gif" />

---

### Инструкция

📝 Для решения задачи отредактируйте файлы: `components/FadeTransition.vue`, `components/FadeTransitionGroup.vue`.

🚀 Команда запуска для ручного тестирования: `npm run serve`;<br>
приложение будет доступно на [http://localhost:8080/06-deep-vue/06-Transitions-1](http://localhost:8080/06-deep-vue/06-Transitions-1).

💬 Задача проверяется вручную на Code Review.