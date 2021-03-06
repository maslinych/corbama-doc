﻿Инструкция по поиску в корпусе
******************************

.. contents:: Содержание

Интерфейс поиска
================

Интерфейс поиска по Справочному корпусу бамана находится в открытом доступе по адресу: http://theschool.spb.ru/bonito/run.cgi/first_form

В открывающемся окне нужно выбрать опцию New query, после чего откроется интерфейс поисковой программы. В его верхней части содержатся три основные опции: Corpus, Query Type, Query.

Подкорпуса
==========

В опции Corpus можно выбрать один из трёх подкорпусов (точнее, двух подкорпусов, по одному из которых возможны два разных типа поиска):

**corbama-brut**
    Подкорпус с неснятой омонимией (на конец июля 2012 имевший объём около 1 100 000 слов);

    Подкорпус corbama-brut даёт существенно больше употреблений каждого слова, но,
    в то же время, и много шума: при автоматическом парсинге текста на бамана с
    опорой на морфологию, порядка 70% всех словоформ текста имеют более одного
    варианта анализа. По сути дела, поиск по этому подкорпусу эквивалентен поиску в
    обычном текстовом редакторе (например, Word), отличаясь лишь большей скоростью
    и удобством представления найденных примеров (в виде конкорданса), а также
    возможностью сохранения результата поиска в различных форматах.

**corbama-net-non-tonal**
    Подкорпус со снятой омонимией (на конец июля 2012 – около 38 000 слов), поиск по которому производится без учёта тонов.

    Поиск по подкорпусу corbama-net позволяет исключить шум и задействовать более
    тонкие параметры за счет снятой омонимии.

    .. note::

        Оговорюсь, что по состоянию на июль 2012, подкорпус со снятой омонимией содержит немалое количество ошибок и непоследовательностей, выявлением и устранением которых рабочая группа занимается. Мы будем благодарны пользователям за сообщения о таких ошибках (можно писать В.Ф.Выдрину, vydrine@gmail.com).

**corbama-net-tonal**
    подкорпус со снятой омонимией (идентичный предыдущему), поиск по которому производится с учётом тонов.

    Тонированный поиск (т.е. поиск по corbama-net-tonal) даёт
    возможность ещё больше уменьшить информационный шум, исключая квазиомонимы,
    отличающиеся от искомой формы тонами.

См. также: :doc:`Правила тональной нотации в Корпусе <tonal-orthography-ru>`.

Аннотация
=========

Все тексты разбиты на токены. **Токен** — это словоформа или знак препинания. Каждой словоформе и каждой морфеме в составе словоформы приписана лингвистическая аннотация.

Все корпуса содержат следующие виды лингвистической аннотации словоформ:

1. **Словоформа** в орфографии бамана 1982 года.

   Если орфография исходного текста иная, то поисковая система даёт примеры в этой исходной орфографии, однако база данных содержит и соответствующую форму в новой орфографии, которая может быть показана при необходимости (см. раздел :ref:`View Options <view_options>`).

   См. также: :doc:`О подходе рабочей группы к вопросу нормализации орфографии в корпусе <orthography-ru>`
2. **Лемма** (или список лемм) — словарная форма для данной словоформы.

   В качестве леммы выступают формы без словоизменительных показателей. Леммами
   считаются также дериваты, образованные от производящих основ с
   лексикализацией, и композиты, образование которых сопровождается
   лексикализацией, т.е. те формы, которые присутствуют в опорной лексической
   базе данных Bamadaba в качестве словарных единиц. В тонированном подкорпусе
   corbama-net-tonal лемма тонирована (т.е. при необозначении тона формы эта
   при поиске по лемме эта форма найдена не будет). В нетонированных
   подкорпусах (corbama-brut, corbama-net-non-tonal) лемма нетонирована
   (соответственно, при поиске по лемме тон указывать не нужно, иначе формы
   найдены не будут). При наличии нескольких фонетических вариантов лексем
   (если это отражено в лексической базе Bamadaba) при поиске по одному из них
   программа находит и те примеры, где эта лексема встретилась в своём втором
   (а также третьем, четвёртом и т.д.) варианте.
3. **Частеречный тэг** (см. :doc:`список принятых в корпусе тегов <pos-tags-ru>`). 
   
   В случае неоднозначности возможные частеречные теги записываются через ``|``.
4. **Глосса** — нормализованный перевод на французский. 
   
   При создании лексической базы данных Bamadaba за основу был взят бамана-французский словарь Шарля Байоля, однако была проведена большая работа по его адаптации с учётом потребности корпусной лексической базы. В частности, каждой лексеме была приписана французская глосса. Если лексема полисемична, для глоссы выбиралось её наиболее прототипическое значение (разумеется, это было не всегда просто, и какие-то решения могут быть в дальнейшем признаны неудовлетворительными и изменены). Иногда глосса представлена двумя или более французскими словами, разделёнными точками (без пробелов), например: ɲɛ̀ɲɛ ‘brisure.de.céréales’, ntòmo ‘fétiche.des.garçons’. Для названий биологических видов (особенно – для тех, которые не имеют общепринятых французских названий) в состав глоссы включается латинское название, которому предшествует слово, обозначающее родовую принадлежность. Например: ɲénu ‘arbre.Hannoa.undulata’, ntómi ‘serpent.Eryx.muelleri’.

   См. также: :doc:`Стандартные глоссы для аффиксов и служебных слов бамана <standard-glosses-ru>`

Типы поиска
===========
В опции Query type (может быть включена и отключена кликом по пункту Query type в меню слева) предлагаются следующие типы поиска:

**Simple**
    По корню, который может совпадать со словоформой или выступать в составе сложной словоформы (в т.ч. деривата или композита) и по целой словоформе.

**Lemma**
    По корню (в т.ч. в составе дериват и композитов) точнее по лемме, т. е. исходной форме слова. При поиске по лемме, в отличие от поиска Simple, не будут отбираться словоформы, в которых искомая последовательность не являет собой один корень. Так, при поиске Simple на стимул sara даются и все употребления глагола sà ‘умирать’ в перфективе (с суффиксом –ra), а при поиске по лемме они не учитываются. Этот тип поиска имеет смысл лишь для подкорпуса со снятой омонимией; при неснятой омонимии его результаты не отличаются от результатов поиска Simple.

**Phrase**
    Поиск по последовательности словоформ, разделённых пробелами (в принципе, здесь можно производить и поиск по одной словоформе, тогда результат будет совпадать с поиском Simple). Этот тип поиска имеет смысл по обоим подкорпусам.

**Word Form**
    Поиск по точной словоформе. В отличие от поиска Simple, при этом не будут найдены те примеры, где корень, представленный данной последовательностью символов, имеет какие-то аффиксы или входит в состав композитов (при поиске по mɔgɔ не будут найдены формы mɔgɔw, dugukɔnɔmɔgɔ, и т.д.). В то же время, будут найдены словоформы сложной морфологичекой структуры (так, при поиске на sara будет учтена и форма перфектива глагола sà). Иначе говоря, этот тип поиска аналогичен поиску в редакторе Word с включённой опцией «только целые слова», а также поиску закавыченного слова при интернет-поиске.

**Character**
    Поиск по последовательности символов (не разделённой пробелами), не обязательно совпадающий с имеющейся в бамана морфемой (корневой или служебной). 

**CQL**
    Поиск по любым параметрам словоформ, а также по комбинациям этих параметров. Наиболее гибкий тип поиска, запросы в котором формулируются на поисковом языке `Corpus Query Language (CQL) <https://trac.sketchengine.co.uk/wiki/SkE/CorpusQuerying>`_ При выборе поиска CQL автоматически появляется окно Default attribute с опциями Word, Lemma, Tag, Gloss. 


Ввод искомой формы
==================

При всех типах поиска, кроме CQL, в окно Query вводится искомая форма, после чего нужно кликнуть на кнопке Make Concordance (внизу экрана) или попросту нажать Enter, после чего программа создаёт конкорданс.

При поиске по **corbama-brut** и **corbama-net-non-tonal** искомые формы не должны содержать обозначений тонов. При поиске по **corbama-net-tonal** искомая форма может быть как :doc:`тонированной <tonal-orthography-ru>`, так и нетонированной.

При поиске типа CQL, в отличие от описанных выше типов, искомая форма заключается в двойные верхние кавычки: ``"kuma"``, ``"dòn"``, ``"pp"``, ``"serpent"``, и т.д.

Комбинированный поиск осуществляется одновременно по разным атрибутам лексемы, что позволяет свести до минимума «шум» и получить более прицельную выборку. При таком поиске неважно, какая опция выбрана в окне Default attribute (поскольку эти же опции задаются в окне CQL «вручную»). Команда, вводимая в окне CQL, имеет следующий синтаксис (при этом содержимое одних квадратных скобок соответствует одному токену)::

    [опция1=”n1” пробел & пробел опция1=”n2”]

(n1, n2 – искомые последовательности знаков).

Например, если мы хотим найти все употребления слова kuma с частеречной пометой «глагол» (v), запрос выглядит следующим образом::

    [word="kuma" & tag="v"]

Возможен и поиск сразу по трём параметрам (или даже четырём, что вряд ли может пригодиться в реальности), например::
    
    [word="kɔnɔ" & tag="n" & gloss="oiseau"]

Очевидным образом, комбинированный поиск целесообразен только по подкорпусу со снятой омонимией.

Комбинированный поиск возможен в CQL и для многословных выражений. При этом каждое слово (точнее, токен) должен помещаться в квадратные скобки, а между токенами должен быть пробел. Например::
    
    [word="bara" & gloss="calebasse"] [word="kɔnɔ" & gloss="à.l’intérieur"]

позволяет найти все сочетания bàra kɔ́nɔ, где первое слово – ‘калебаса’ (а не ‘chez’, ‘dancing’, ‘préféré’), а второе – инэссивный послелог (а не ‘attendre’, ‘bouton.de.fleur’, ‘oisezu’, ‘ventre’).

В режиме CQL возможен поиск по грамматическому шаблону, который может быть полезен для синтсксических исследований. Например, поисковое выражение::
    
    [tag="n"] [tag="adv"] [tag="v"]

должно выявить случаи употребления предглагольных наречий с переходными глаголами. А если такие случаи не находятся, это свидетельствует или о редкости таких наречий в текстах, или (более вероятно) об ошибках операторов снятия омонимии.

Режим CQL позволяет осуществлять поиск редупликатов (отсутствующих в словаре Bamadaba). Если пользователю нужны все редуплицированные глаголы, вводится следующая команда::

    1:[tag="v"] 2:[tag="v"] & 1.word = 2.word

Если он хочет найти все редуплицированные слова в корпусе, команда должна иметь следующий вид::

    1:[] 2:[] & 1.word = 2.word

Уточним, что эти команды позволяют найти редупликаты, написанные раздельно. Если же нам нужны редуплицированные формы, написанные слитно, команда должна выглядеть так::

    "(.+)\1"

Для поиска форм, напсанных через дефис, даём такую команду::

    "(.+)-\1"

Если мы хотим получить сразу и слитные, и дефисные написания, запрашиваем так::

    "(.+)-?\1"

Чтобы уменьшить шум, можно исключить из поиска ненужные символы (цифры, знак %, и т.п.); они перечисляются без пробелов, помещаясь в квадратные скобки перез знаком +, при этом им предшествует знак ^. Таким образом, команда «найти все редуплицированные формы, написанные слитно или через дефис, исключив из поиска цифры и знак %», выглядит так::

    "([^0-9%]+)-?\1"


Ввод нестандартных символов
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ввод нестандартных символов (ɔ, ɛ, ŋ, ɲ, тональных диакритик) возможен двумя способами:

1. При помощи любых клавиатурных раскладок, предназначенных для такого ввода (при этом может быть использована, например, и обычная французская клавиатура – для à, è, é, ù… – другое дело, что далеко не всё необходимое можно с её помощью набрать);
2. Эти нестандартные символы можно заменять следующими комбинациями::

    ;o = ɔ
    ;e = ɛ
    ;n = ŋ
    ;m = ɲ

Знак высокого тона (акут) при этом заменяется запятой, стоящей после соответствующей гласной; знак низкого тона – развёрнутым апострофом. Программа автоматически преобразует эти сочетания в нужные символы, например::

    k;o, -> kɔ́
    su` -> sù
    k;e,n;e -> kɛ́nɛ
    ;m;o` -> ɲɔ̀
    ;n;o`mi -> ŋɔ̀mi.

Опция Context
=============

Эта опция позволяет осуществлять поиск сочетания дистантно расположенных форм. Она может быть включена и отключена нажатием на Context в меню слева.

В окне Query указывается опорная форма (та, по отношению к которой задаётся контекст).

В Lemma filter – Lemma указывается интересующая пользователя контекстная форма (т.е. та форма, сочетания с которой с опорной формой требуется найти; тут может быть и более одной формы).

В Lemma filter – Windows можно указать, какой контекст нас интересует (left, right, both – в последнем случае учитывается и правый, и левый контекст), справа предлагается указать протяжённость контекста, который принимается во внимание (от 1 до 15 форм). Если задаётся протяжённость 1, то поисковик найдёт только формы, непосредственно прилегающие к опорной (т.е. результат будет аналогичен тому, который мы получим при поиске типа Phrase). При протяжённости контекста равной 2, будут найдены формы, как непосредственно примыкающие к опорной, так и те, которые отделены от неё какой-либо одной формой, и т.д. (при этом контекстная форма может быть отделена от опорной и границей предложения).

Справа от окна Lemma расположено окно с опциями All, Any, None. 

Если выбрана опция All, при этом в окне Lemma внесены две (или более) контекстные формы, то поисковик найдёт только те примеры, где присутствуют все три формы (опорная и обе контекстные). Например, при опорной форме kɛ и двух контекстных – yɛrɛ, ɲɔgɔn, будут найдены такие примеры:

|    Mɔgɔ min bɛ a mɔgɔɲɔgɔn jogin , a ye min kɛ o tigi la , o **ɲɔgɔn** ka **kɛ** a **yɛrɛ** fana la .
|    O de bɛ cikɛla kɛ senyɛrɛkɔrɔbaga ye , i n' a fɔ birokɔnɔbaarakɛla ; i n' a fɔ taɲini julabaw , i n' a fɔ **yɛrɛ** jamanakuntigi n' a **kokɛɲɔgɔnw** , senyɛrɛkɔrɔ siratɛgɛ la 
|    **Jatigikɛ** **yɛrɛ** ɲuman na , a **ɲɔgɔn** cɛ kisɛ t' ale denw na .
|    и т.д.

Такой поиск может быть весьма эффективен для проверки возможности употребления переходных глаголов с различными предикативными показателями (скажем, при изучении акциональных классов), при изучении сочетаний глаголов с послелогами, и т.п.

При включённой опции Any, будут найдены все случаи совместного употребления морфемы kɛ с хотя бы одним из двух контекстных форм (в том числе, разумеется, и те случаи, когда присутствуют обе контекстные формы).

При включённой опции None программа выдаст все случаи употребления опорного слова, когда на заданной дистанции **отсутствуют** контекстные формы. Эта опция может быть полезной, когда некая форма обычно употребляется в составе каких-то устойчивых выражений, а пользователя интересуют её употребления вне таких выражений.

Text types
==========

Этот пункт меню позволяет ограничить набор текстов, по которым производится поиск. Опция может быть включена и отключена нажатием на Text types в меню слева.

По умолчанию, поисковая программа ищет по всему подкорпусу. В первом окне, doc.id, можно задать искомый текст; для этого нужно начать набирать фамилию его автора или первое слово произведения. Если в названиях файлов эти элементы присутствуют, то эти названия будут подсказаны во всплывающей подсказке.

Ниже расположено окно doc.text_genre, в котором можно задать ограничения по жанровым характеристикам текстов.
В дальнейшем планируется возможность ограничения подкорпуса для поиска и по другим параметром.

Concordance
===========

Неотрицательным результатом поиска по корпусу является конкорданс, т.е. список всех примеров (с их контекстами), найденных в корпусе (или подкорпусе). Справочный корпус бамана не имеет ограничений по количеству предоставляемых пользователю примеров. В верхней белой полосе указано количество найденных примеров (Hits). Под этой полосой указывается количество страниц (если число найденных примеров более 20; по умолчанию, на одной странице даётся по 20 примеров), здесь же расположены кнопки навигации по конкордансу.

Для каждого примера указывается название файла (в названии файла отражены,
достаточно прозрачно, имя автора и название текста; см. подробнее :doc:`о правилах именования файлов <file-naming-ru>`.

Полученный конкорданс может быть сохранён по частями или целиком в текстовом формате. Для сохранения целиком нужно выбрать опцию Save в меню слева.

Для настройки формы представления конкорданса в меню имеются две опции  – KWIC/Sentence и View Options.

Нажатием на KWIC/Sentence производится простое переключение режима просмотра примеров: Sentence – показывается целое предложение («от точки до точки»), содержащее искомую форму; KWIC – показывается правый и левый контекст заданного размера (по умолчанию, 40 знаков слева и 40 знаков справа от искомой формы).

.. _view_options:

Опция View Options позволяет регулировать представление конкорданса более детально. В интерфейсе View Options можно:

* изменить атрибуты формы (Attributes) – если пометить опции word, lemma, tag, gloss, то соответствующие атрибуты (лемма, частеречная помета, французская глосса; по умолчанию, опция word помечена всегда) при форме будут указаны;
* указать, должны ли эти атрибуты указываться при каждом слове каждого примера, или только при искомом слове (раздел Display Attributes). 

Отметим, что в настоящее время все артибуты формы даются линейно, через слэш. Такое представление оказывается несколько громоздким для подкорпуса с неснятой омонимией (corbama.brut), поскольку атрибуты указываются для каждого варианта разбора словоформы, а таких вариантов может быть несколько. Особенно неудобочитаемым оказывается в этом подкорпусе представление атрибутов для всех слов (Display attributes – For each token). По-видимому, использование этой опции следует признать целесообразной только для подкорпуса со снятой омонимией.

Ниже можно установить, сколько примеров должно быть показано на одной странице (Page size; по умолчанию, выставляется цифра 20); каков размер правого и левого контекста (KWIC Context size; в принципе, он может быть увеличен до бесконечности, но по умочанию выставляется цифра 40).

Остальные функции раздела View Options (Sort good dictionary examples и т.д.) для нашего корпуса нерелвантны.

Сортировка примеров регулируется в опции Sorting. Примеры могут следовать а алфавитном порядке формы, располагающейся справа от искомого (Right context) или слева от искомого (Left context), при этом различие прописных и строчных букв может учитываться или игнорироваться (Ignore case). Возможно также выстраивание в обратном алфавитном порядке (Backward). Приведение в действие выбранных параметров производится нажатием кнопки Sort Concordance.

Многоуровневая сортировка для нашего корпуса пока что неактуальна.

В общем меню содержатся также опции Sorting – References (сортировка по именам файлов, в которых найдены искомые формы) и Sorting – Shuffle (перемешивание примеров, в результате которого они располагаются в случайном порядке).

Опция Sample позволяет делать случайную выборку заданного размера из числа всех найденных в корпусе примеров.

Опция Filter аналогична по своим функциям опции Context, описанной выше (раздел 4).

Опция Frequency даёт доступ к статистике словоформ, в состав которых входит искомый элемент, а также статистики его сочетаемости с соседними формами.

В интерфейсе этой опции есть два раздела. 

1. Multilevel frequency distribution. Для каждого уровня иерархии сортировки по частоте нужно выбрать:

   * Node, и тогда подсчитывается частота словоформ, в которые входит искомый элемент (при этом можно выбрать опцию Ignore case, тогда не будет учитываться различие между прописными и строчными буквами),
   *  элементы из левого контекста (1L, 2L, 3L… – в зависимости от протяжённости контекста) или правого контекста (1R, 2R, 3R…). Тогда будет подсчитана частота сочетаемости с формами слева или справа.

   При этом могут задаваться атрибуты опорного или контекстного элемента: word,
   lemma, tag, gloss. Отметим, что при подсчёте частот по корпусу с неснятой
   омонимией (corbama-brut) выяснение частот опорного элемента по параметрам
   lemma, tag, gloss нерелевантна.

2. Раздел Text Type frequency distribution позволяет определить частоту встречаемости искомого элемента в:

   * разных файлах, опция doc.id;
   * разных текстах (отметим, что один текст может быть представлен в Корпусе несколькими файлами), опция doc.text_title;
   * текстах разного жанра, опция doc.text_genre.

Раздел Collocations позволяет определить возможные устойчивые сочетания с искомым словом. Возможен поиск сочетаемости по атрибутам (Attribute) соседних элементов (word, lemma, tag, gloss), при этом можно учитывать только элементы левого контекста (In the range from -1, -2, etc.) или правого контекста (… to 1, 2, etc.); цифровые значения соответствуют протяжённости контекста (-1/1: учитывается только непосредственно примыкающий сосед; -2/2: учитываются ближайший сосед и непосредственно предшествующее/непосредственно следующее за ним слово, и т.д.).

Нажав кнопку Make Candidate List, получаем список кандидатов на устойчивые сочетания. Их можно выстроить в порядке убывания частоты, кликнув по голубой этикетке Frec.

Word List
=========

Опция Word List позволяет создавать частотный словарь. Если войти в эту опцию, то в меню слева появляются эктикетки All words , All lemmas. Нажав на эти кнопки, мы получаем частотный список (в порядке убывания) всех токенов по данному подкорпусу (поскольку знаки препинания тоже имеют статус токенов, они фигурируют в этом списке наряду со словами).
