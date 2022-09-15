# Стиль кода для юнити проектов
**C# | Unity. Code style, arhitecture**

***Всем привет!***
Тут я кратко опишу правила для совместной работы над кодом в юнити проекте.

# Наименование

Я придерживаюсь правил от *майков и .net разработчиков*.

https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions

https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/coding-style.md

Каждый класс должен быть обернут в *namespace*.

Плохое название для *namespace*:

**namespace Assets.Scripts.MonoBehaviour.Hero**

Хорошее название для *namespace*:

**namespace Sources.HeroLogic**

*Visual studio* по дефолту добавляет приписку *Assets* к *namespace*, но она не имеет смысла.

***Немного о папочках***

Лучше не использовать для папки с кодом название *Scripts*. Я решила использовать название *Sources*. В примере с плохим *namespace'ом* написано *Scripts* что является ошибкой. Опять же этот *namespace* создан автоматический с помощью *Visual studio*. В *Rider* такой проблемы вроде как нет.

Также лучше не использовать в *namespace'е* название *MonoBehaviour* ( ***только MonoBehaviourS*** ).

В конце *namespace'a* лучше делать приписку ***Logic***. Иначе если название класса и *namespace'а* будет совпадать, то будет ошибка.

# Папки

Я придерживаюсь этого:

- Assets
  - Sources
    - MonoBehaviours ( классы наследующие MonoBehaviour )
      - Hero
      - Door
      - Enemy
      - Items
      - UI
        - LoadingScreen
        - Shop
        - MainMenu
    - Arhitecture
      - Bootstrapper  
      - Services
      - StateMachine
      - И подобные вещи 
    - Другие папки. Зависит случая
  - Content
    - Art ( 2д контент )
    - Models ( Меши, Текстуры, Анимации в одной папке )
    - Sound
    - Animations
    - Scenes
      - Users ( папки каждого человека на которой он делает что хочет )
      - Game ( игра )
        - MainMenu
        - House
        - Outside
      - DebugGame ( Не уверена нужно ли оно или нет, но идея в том, что Game - релиз, а DebugGame - дебаг )          
    - Materials ( в папке материала находятся текстуры и все вещи для него )
    - И так далее  
  - Plugins
    - Zenject
    - UniRx
    - DoTween 
