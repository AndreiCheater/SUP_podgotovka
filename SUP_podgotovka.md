# Подготовка к экзамену по дисциплине СУП

**Тема:** Следящие электроприводы

---

## 1. Следящие электроприводы. Общие сведения

Следящий электропривод — это замкнутая электромеханическая система управления электроприводом (СУЭП), в которой выходное перемещение должно повторять (отслеживать) произвольно изменяющееся входное (задающее) воздействие.

**Классификация:**
- **Непрерывные**
- **Дискретные**, которые делятся на:
  - релейные
  - импульсные

Устройства автоматического управления в следящих системах могут быть реализованы на различных элементах: электронных (полупроводниковых), магнитных, электромашинных, гидравлических и пневматических.

Для обеспечения заданных показателей качества применяются все возможные законы регулирования: от пропорционального (П) до пропорционально-интегрально-дифференциального (ПИД). Может использоваться также принцип комбинированного управления с компенсацией возмущающего воздействия.

---

## 2. Основные требования к следящим электроприводам

К следящим электроприводам предъявляются следующие основные требования:

а) **Высокая точность** воспроизведения задающего воздействия в статике и переходных режимах;

б) **Устойчивость** во всём диапазоне скоростей;

в) **Высокое быстродействие**;

г) **Малая колебательность**;

д) **Простота реализации и надёжность** в работе.

**Мнемоника для запоминания: «ТУБКП»** — Точность, Устойчивость, Быстродействие, Колебательность малая, Простота.

---

## 3. Следящий электропривод с непрерывным управлением

Для измерения угла рассогласования θ = θ_вх − θ_вых используются **сельсин-датчик (СД)** и **сельсин-приёмник (СП)**, включённые по трансформаторной схеме. Ротор СД соединён с задающим валом, а ротор СП — с выходным валом электродвигателя М.

**Функциональная схема:**

```svg
<svg width="100%" viewBox="0 0 680 340" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arr3" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse"><path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></marker>
</defs>

<text x="40" y="30" font-family="sans-serif" font-size="12" fill="#5F5E5A">Задающий вал θвх</text>
<line x1="40" y1="60" x2="100" y2="60" stroke="#5F5E5A" stroke-width="2"/>
<circle cx="40" cy="60" r="4" fill="#5F5E5A"/>

<rect x="100" y="40" width="90" height="44" rx="6" fill="#E6F1FB" stroke="#185FA5" stroke-width="0.5"/>
<text x="145" y="67" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#0C447C">СД</text>

<line x1="190" y1="62" x2="240" y2="62" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr3)"/>
<text x="215" y="55" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">3-фаз.</text>

<rect x="240" y="40" width="90" height="44" rx="6" fill="#E6F1FB" stroke="#185FA5" stroke-width="0.5"/>
<text x="285" y="67" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#0C447C">СП</text>

<line x1="285" y1="84" x2="285" y2="120" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr3)"/>
<text x="345" y="105" font-family="sans-serif" font-size="12" fill="#5F5E5A">Uθ = Um·sin θ</text>

<rect x="240" y="120" width="90" height="44" rx="6" fill="#EEEDFE" stroke="#534AB7" stroke-width="0.5"/>
<text x="285" y="147" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#3C3489">ФЧУ</text>

<line x1="285" y1="164" x2="285" y2="200" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr3)"/>
<text x="325" y="185" font-family="sans-serif" font-size="12" fill="#5F5E5A">Uвых</text>

<rect x="240" y="200" width="90" height="44" rx="6" fill="#EEEDFE" stroke="#534AB7" stroke-width="0.5"/>
<text x="285" y="223" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#3C3489">ЭМУ</text>
<text x="285" y="238" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#3C3489">(ОУ)</text>

<line x1="330" y1="222" x2="390" y2="222" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr3)"/>
<text x="360" y="215" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">U</text>

<rect x="390" y="200" width="90" height="44" rx="6" fill="#E1F5EE" stroke="#0F6E56" stroke-width="0.5"/>
<text x="435" y="227" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#085041">М</text>

<line x1="480" y1="222" x2="540" y2="222" stroke="#5F5E5A" stroke-width="2"/>
<line x1="540" y1="222" x2="540" y2="62" stroke="#5F5E5A" stroke-width="2" stroke-dasharray="4 4"/>
<line x1="540" y1="62" x2="330" y2="62" stroke="#5F5E5A" stroke-width="1.5" stroke-dasharray="4 4" fill="none" marker-end="url(#arr3)"/>
<text x="555" y="145" font-family="sans-serif" font-size="12" fill="#5F5E5A">мех. связь</text>

<text x="550" y="215" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвых</text>
<circle cx="540" cy="222" r="4" fill="#5F5E5A"/>
<text x="555" y="240" font-family="sans-serif" font-size="12" fill="#5F5E5A">Выходной вал</text>

<text x="40" y="290" font-family="sans-serif" font-size="12" fill="#5F5E5A">СД — сельсин-датчик, СП — сельсин-приёмник</text>
<text x="40" y="310" font-family="sans-serif" font-size="12" fill="#5F5E5A">ФЧУ — фазочувствительный усилитель, ЭМУ — электромашинный усилитель, М — двигатель</text>
</svg>
```

**Принцип работы:**

При согласованном положении роторов (θ_вх = θ_вых) выходное напряжение U_θ, снимаемое с однофазной обмотки СП, равно нулю. Соответственно равны нулю напряжение U_вых на управляющей обмотке ОУ электромашинного усилителя и напряжение U питания электродвигателя.

При повороте задающего вала на выходе СП появляется напряжение:

$$U_\theta = U_m \cdot \sin\theta$$

Фаза этого напряжения зависит от знака угла рассогласования θ. На выходе фазочувствительного усилителя (ФЧУ) появляется напряжение U_вых соответствующей полярности. Появляется напряжение U на электродвигателе М, и он поворачивает выходной вал и вместе с ним ротор СП до согласованного положения роторов.

Таким образом, выходной силовой вал повторяет перемещение задающего вала.

---

## 4. Релейный следящий электропривод

Узел измерения угла рассогласования θ = θ_вх − θ_вых выполнен на **потенциометрах П1 и П2**. При одинаковых положениях движков потенциометров (θ_вх = θ_вых) напряжения U_вх и U_вых одинаковы, а напряжение U_θ = U_вх − U_вых на входе электронного усилителя (ЭУ) равно нулю.

**Функциональная схема:**

```svg
<svg width="100%" viewBox="0 0 680 340" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arr4" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse"><path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></marker>
</defs>

<text x="40" y="30" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвх</text>
<circle cx="55" cy="45" r="4" fill="#5F5E5A"/>

<rect x="40" y="55" width="90" height="44" rx="6" fill="#E6F1FB" stroke="#185FA5" stroke-width="0.5"/>
<text x="85" y="82" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#0C447C">П1</text>

<line x1="130" y1="77" x2="200" y2="77" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr4)"/>
<text x="165" y="70" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">Uвх</text>

<rect x="200" y="55" width="90" height="44" rx="6" fill="#EEEDFE" stroke="#534AB7" stroke-width="0.5"/>
<text x="245" y="77" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#3C3489">ЭУ</text>
<text x="245" y="93" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#3C3489">усилитель</text>

<line x1="290" y1="77" x2="360" y2="77" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr4)"/>
<text x="325" y="70" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">Uвых</text>

<rect x="360" y="40" width="70" height="34" rx="6" fill="#FAEEDA" stroke="#854F0B" stroke-width="0.5"/>
<text x="395" y="62" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#633806">К1</text>

<rect x="360" y="82" width="70" height="34" rx="6" fill="#FAEEDA" stroke="#854F0B" stroke-width="0.5"/>
<text x="395" y="104" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#633806">К2</text>

<line x1="430" y1="57" x2="480" y2="70" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr4)"/>
<line x1="430" y1="99" x2="480" y2="85" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr4)"/>

<rect x="480" y="55" width="90" height="44" rx="6" fill="#E1F5EE" stroke="#0F6E56" stroke-width="0.5"/>
<text x="525" y="82" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#085041">М</text>

<line x1="570" y1="77" x2="620" y2="77" stroke="#5F5E5A" stroke-width="2"/>
<text x="600" y="70" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвых</text>

<line x1="600" y1="77" x2="600" y2="180" stroke="#5F5E5A" stroke-width="2" stroke-dasharray="4 4"/>
<line x1="600" y1="180" x2="85" y2="180" stroke="#5F5E5A" stroke-width="2" stroke-dasharray="4 4"/>
<line x1="85" y1="180" x2="85" y2="195" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr4)"/>
<text x="330" y="172" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">обратная связь (мех.)</text>

<rect x="40" y="195" width="90" height="44" rx="6" fill="#E6F1FB" stroke="#185FA5" stroke-width="0.5"/>
<text x="85" y="222" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#0C447C">П2</text>

<line x1="85" y1="239" x2="85" y2="260" stroke="#5F5E5A" stroke-width="2"/>
<line x1="85" y1="260" x2="245" y2="260" stroke="#5F5E5A" stroke-width="2"/>
<line x1="245" y1="260" x2="245" y2="99" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr4)"/>
<text x="165" y="275" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">Uθ = Uвх − Uвых</text>

<text x="40" y="310" font-family="sans-serif" font-size="12" fill="#5F5E5A">П1, П2 — задающий и обратной связи потенциометры. К1, К2 — электромагнитные реле</text>
</svg>
```

**Принцип работы:**

При повороте движка задающего потенциометра П1 на входе ЭУ появляется напряжение U_θ, пропорциональное углу рассогласования θ = θ_вх − θ_вых, полярность которого зависит от знака угла рассогласования.

Появляется напряжение соответствующей полярности U_вых на выходе ЭУ, срабатывает одно из электромагнитных реле К1 или К2 и подаёт напряжение на электродвигатель М постоянного тока с двумя последовательными обмотками возбуждения. Двигатель поворачивает выходной вал и движок потенциометра П2 обратной связи до согласованного положения движков П1 и П2.

---

## 5. Импульсный следящий электропривод

При согласованном положении движков задающего потенциометра П1 и потенциометра обратной связи П2 напряжение U_θ = 0. Под действием напряжения U_Т вторичной обмотки трансформатора TV поляризованное реле К попеременно замыкает контакты К1, К2 и К3, К4, подавая на электродвигатель М напряжение одной и другой полярности. При этом продолжительности импульсов t₁ и t₂ одинаковы и двигатель неподвижен.

**Графики напряжений:**

```svg
<svg width="100%" viewBox="0 0 680 480" xmlns="http://www.w3.org/2000/svg">
<text x="40" y="30" font-family="sans-serif" font-size="14" font-weight="500" fill="#2C2C2A">а) UT — напряжение на вторичной обмотке трансформатора</text>
<line x1="40" y1="90" x2="640" y2="90" stroke="#5F5E5A" stroke-width="1"/>
<line x1="60" y1="50" x2="60" y2="130" stroke="#5F5E5A" stroke-width="1"/>
<text x="45" y="55" font-family="sans-serif" font-size="12" fill="#5F5E5A">U</text>
<text x="630" y="105" font-family="sans-serif" font-size="12" fill="#5F5E5A">t</text>

<path d="M60 90 Q90 50 120 90 Q150 130 180 90 Q210 50 240 90 Q270 130 300 90 Q330 50 360 90 Q390 130 420 90 Q450 50 480 90 Q510 130 540 90 Q570 50 600 90" fill="none" stroke="#185FA5" stroke-width="1.5"/>

<text x="40" y="170" font-family="sans-serif" font-size="14" font-weight="500" fill="#2C2C2A">б) UК при согласованном положении (Uθ = 0): t1 = t2</text>
<line x1="40" y1="230" x2="640" y2="230" stroke="#5F5E5A" stroke-width="1"/>
<line x1="60" y1="190" x2="60" y2="270" stroke="#5F5E5A" stroke-width="1"/>

<rect x="60" y="200" width="60" height="30" fill="#0F6E56" opacity="0.8"/>
<rect x="120" y="230" width="60" height="30" fill="#993C1D" opacity="0.8"/>
<rect x="180" y="200" width="60" height="30" fill="#0F6E56" opacity="0.8"/>
<rect x="240" y="230" width="60" height="30" fill="#993C1D" opacity="0.8"/>
<rect x="300" y="200" width="60" height="30" fill="#0F6E56" opacity="0.8"/>
<rect x="360" y="230" width="60" height="30" fill="#993C1D" opacity="0.8"/>
<rect x="420" y="200" width="60" height="30" fill="#0F6E56" opacity="0.8"/>
<rect x="480" y="230" width="60" height="30" fill="#993C1D" opacity="0.8"/>
<rect x="540" y="200" width="60" height="30" fill="#0F6E56" opacity="0.8"/>

<text x="90" y="195" font-family="sans-serif" font-size="12" fill="#5F5E5A">t1</text>
<text x="150" y="275" font-family="sans-serif" font-size="12" fill="#5F5E5A">t2</text>

<text x="40" y="310" font-family="sans-serif" font-size="14" font-weight="500" fill="#2C2C2A">в) UМ при θ ≠ 0: t1 &gt; t2 — двигатель поворачивается</text>
<line x1="40" y1="380" x2="640" y2="380" stroke="#5F5E5A" stroke-width="1"/>
<line x1="60" y1="330" x2="60" y2="430" stroke="#5F5E5A" stroke-width="1"/>

<rect x="60" y="340" width="90" height="40" fill="#0F6E56" opacity="0.8"/>
<rect x="150" y="380" width="30" height="40" fill="#993C1D" opacity="0.8"/>
<rect x="180" y="340" width="90" height="40" fill="#0F6E56" opacity="0.8"/>
<rect x="270" y="380" width="30" height="40" fill="#993C1D" opacity="0.8"/>
<rect x="300" y="340" width="90" height="40" fill="#0F6E56" opacity="0.8"/>
<rect x="390" y="380" width="30" height="40" fill="#993C1D" opacity="0.8"/>
<rect x="420" y="340" width="90" height="40" fill="#0F6E56" opacity="0.8"/>
<rect x="510" y="380" width="30" height="40" fill="#993C1D" opacity="0.8"/>
<rect x="540" y="340" width="90" height="40" fill="#0F6E56" opacity="0.8"/>

<text x="105" y="335" font-family="sans-serif" font-size="12" fill="#5F5E5A">t1 (увеличилось)</text>
<text x="165" y="440" font-family="sans-serif" font-size="12" fill="#5F5E5A">t2 (уменьшилось)</text>

<text x="40" y="465" font-family="sans-serif" font-size="12" fill="#5F5E5A">Среднее напряжение на двигателе отлично от нуля → М поворачивает выходной вал</text>
</svg>
```

**При появлении угла рассогласования:**

При появлении угла рассогласования θ = θ_вх − θ_вых и напряжения U_θ соответствующей полярности реле переключается под действием суммарного напряжения:

$$U_К = U_Т + U_\theta$$

Продолжительность импульсов одной полярности увеличивается, другой — уменьшается, и двигатель поворачивает выходной вал до устранения угла рассогласования θ.

В современных импульсных следящих электроприводах вместо поляризованного реле применяются полупроводниковые **широтно-импульсные модуляторы (ШИМ)** напряжения питания электродвигателя на транзисторах или тиристорах.

---

## 6. Следящий электропривод с шаговым электродвигателем

Данный вариант электропривода получает в последнее время всё более широкое применение.

**Устройство:** Шаговый двигатель ШД получает питание от тиристорного или транзисторного коммутатора К и поворачивает выходной вал дискретно с фиксированным шагом с частотой, определяемой тактовой частотой f задающего генератора Г.

**Функциональная схема:**

```svg
<svg width="100%" viewBox="0 0 680 240" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arr6" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse"><path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></marker>
</defs>

<text x="30" y="75" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвх</text>
<line x1="30" y1="90" x2="60" y2="90" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr6)"/>

<rect x="60" y="70" width="90" height="44" rx="6" fill="#E6F1FB" stroke="#185FA5" stroke-width="0.5"/>
<text x="105" y="97" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#0C447C">ЗЭ</text>

<line x1="150" y1="92" x2="200" y2="92" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr6)"/>
<text x="175" y="85" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">N имп.</text>

<rect x="200" y="70" width="100" height="44" rx="6" fill="#EEEDFE" stroke="#534AB7" stroke-width="0.5"/>
<text x="250" y="92" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#3C3489">Г</text>
<text x="250" y="108" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#3C3489">частота f</text>

<line x1="300" y1="92" x2="340" y2="92" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr6)"/>

<rect x="340" y="70" width="90" height="44" rx="6" fill="#EEEDFE" stroke="#534AB7" stroke-width="0.5"/>
<text x="385" y="92" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#3C3489">К</text>
<text x="385" y="108" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#3C3489">коммутатор</text>

<line x1="430" y1="92" x2="470" y2="92" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr6)"/>

<rect x="470" y="70" width="90" height="44" rx="6" fill="#E1F5EE" stroke="#0F6E56" stroke-width="0.5"/>
<text x="515" y="97" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#085041">ШД</text>

<line x1="560" y1="92" x2="600" y2="92" stroke="#5F5E5A" stroke-width="2"/>

<rect x="600" y="70" width="60" height="44" rx="6" fill="#F1EFE8" stroke="#5F5E5A" stroke-width="0.5"/>
<text x="630" y="97" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#2C2C2A">УО</text>

<text x="595" y="135" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвых = θвх</text>

<text x="30" y="180" font-family="sans-serif" font-size="12" fill="#5F5E5A">Принцип разомкнутого управления по жёсткой программе</text>
<text x="30" y="200" font-family="sans-serif" font-size="12" fill="#5F5E5A">ЗЭ — задающий элемент, Г — генератор, К — коммутатор, ШД — шаговый двигатель, УО — управляемый объект</text>
</svg>
```

**Особенности:**

Это позволяет строить следящую систему без контура обратной связи (**принцип разомкнутого управления по жёсткой программе**).

Задающий элемент ЗЭ преобразует угол поворота задающего вала θ_вх в пропорциональное количество импульсов тактового генератора, и электродвигатель ШД поворачивает выходной вал управляемого объекта УО на соответствующее число шагов, так что θ_вых = θ_вх.

Для повышения точности слежения в переходных режимах используются замкнутые системы управления по отклонению.

---

## 7. Следящий электропривод с обратной связью по выходной величине с П-регулятором

**Допущения:** Регулятор Р пропорциональный, преобразователь П линейный безынерционный с выходным сопротивлением R_п = 0. Электромагнитная постоянная времени якорной цепи двигателя Т_я мала по сравнению с электромеханической Т_м и ею можно пренебречь.

**Структурная схема:**

```svg
<svg width="100%" viewBox="0 0 680 260" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arr7" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse"><path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></marker>
</defs>

<text x="20" y="85" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвх</text>
<line x1="20" y1="100" x2="60" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr7)"/>

<rect x="60" y="80" width="50" height="40" rx="6" fill="#E6F1FB" stroke="#185FA5" stroke-width="0.5"/>
<text x="85" y="105" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#0C447C">П1</text>

<line x1="110" y1="100" x2="145" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr7)"/>

<circle cx="160" cy="100" r="14" fill="none" stroke="#5F5E5A" stroke-width="1"/>
<line x1="150" y1="100" x2="170" y2="100" stroke="#5F5E5A"/>
<line x1="160" y1="90" x2="160" y2="110" stroke="#5F5E5A"/>
<text x="145" y="80" font-family="sans-serif" font-size="12" fill="#5F5E5A">+</text>
<text x="170" y="125" font-family="sans-serif" font-size="12" fill="#5F5E5A">−</text>

<line x1="174" y1="100" x2="210" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr7)"/>
<text x="192" y="90" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">θ</text>

<rect x="210" y="80" width="60" height="40" rx="6" fill="#EEEDFE" stroke="#534AB7" stroke-width="0.5"/>
<text x="240" y="105" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#3C3489">Р</text>

<line x1="270" y1="100" x2="310" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr7)"/>

<rect x="310" y="80" width="60" height="40" rx="6" fill="#EEEDFE" stroke="#534AB7" stroke-width="0.5"/>
<text x="340" y="105" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#3C3489">П</text>

<line x1="370" y1="100" x2="405" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr7)"/>
<text x="387" y="90" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">Uм</text>

<rect x="405" y="80" width="70" height="40" rx="6" fill="#E1F5EE" stroke="#0F6E56" stroke-width="0.5"/>
<text x="440" y="105" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#085041">М</text>

<line x1="475" y1="100" x2="515" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr7)"/>
<text x="495" y="90" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">ω</text>

<rect x="515" y="80" width="60" height="40" rx="6" fill="#F1EFE8" stroke="#5F5E5A" stroke-width="0.5"/>
<text x="545" y="105" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#2C2C2A">1/p</text>

<line x1="575" y1="100" x2="640" y2="100" stroke="#5F5E5A" stroke-width="2"/>
<text x="615" y="90" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвых</text>
<circle cx="620" cy="100" r="3" fill="#5F5E5A"/>

<line x1="620" y1="100" x2="620" y2="180" stroke="#5F5E5A" stroke-width="1.5" stroke-dasharray="4 4"/>
<line x1="620" y1="180" x2="130" y2="180" stroke="#5F5E5A" stroke-width="1.5" stroke-dasharray="4 4"/>
<line x1="130" y1="180" x2="130" y2="200" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr7)"/>

<rect x="105" y="200" width="50" height="40" rx="6" fill="#E6F1FB" stroke="#185FA5" stroke-width="0.5"/>
<text x="130" y="225" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#0C447C">П2</text>

<line x1="155" y1="220" x2="175" y2="220" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="175" y1="220" x2="175" y2="114" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr7)"/>

<text x="370" y="190" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">обратная связь по θвых</text>
</svg>
```

**Система уравнений (6.1):**

$$U_м = K_1 \cdot K_р \cdot K_п \cdot \theta, \quad \theta = \theta_{вх} - \theta_{вых}$$

$$i = \frac{U_м - C_E \cdot \omega}{R_a}$$

$$J \cdot p \cdot \omega = C_E \cdot (i - i_c)$$

$$\omega = p \cdot \theta_{вых}$$

**Итоговое уравнение (6.2):**

$$\theta(t) = \frac{p(T_м \cdot p + 1)}{T_м \cdot p^2 + p + K} \cdot \theta_{вх}(t) + \frac{1}{T_м \cdot p^2 + p + K} \cdot \frac{M_c}{b}$$

где:
- K = K₁·K_р·K_п·(1/C_E) — общий коэффициент усиления разомкнутой системы
- b = C_E²/R_a — жёсткость механической характеристики двигателя
- T_м = J/b — электромеханическая постоянная времени двигателя

**Статическая ошибка** (при p = 0):

$$\theta_{ст} = \frac{M_c}{K \cdot b}$$

Она пропорциональна нагрузке на валу двигателя и обратно пропорциональна жёсткости механической характеристики и величине K общего коэффициента усиления разомкнутой системы.

**Скоростная ошибка** (при p·θ_вх = Ω_вх = const):

$$\theta_{ск} = \frac{\Omega_{вх}}{K}$$

**Характеристическое уравнение:**

$$T_м \cdot p^2 + p + K = 0$$

$$p_{1,2} = -\frac{1}{2T_м} \pm \frac{1}{2T_м}\sqrt{1 - 4KT_м}$$

При K > 1/(4T_м) переходной процесс будет колебательным, причём увеличение K ведёт к росту амплитуды колебаний и времени регулирования, что затрудняет возможность повышения таким путём точности слежения.

---

## 8. Следящий электропривод с дополнительной обратной связью по первой и второй производным от выходной величины

### Обратная связь по первой производной

Для получения обратной связи по первой производной от угла поворота выходного вала используют **тахогенератор**, выходное напряжение которого U_тг = K_c·ω_вых = K_c·p·θ_вых вычитают из напряжения U_θ = K₁·θ.

**Структурная схема с ОС по производным:**

```svg
<svg width="100%" viewBox="0 0 680 320" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arr8" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse"><path d="M2 1L8 5L2 9" fill="none" stroke="context-stroke" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></marker>
</defs>

<text x="20" y="85" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвх</text>
<line x1="20" y1="100" x2="50" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr8)"/>

<circle cx="65" cy="100" r="14" fill="none" stroke="#5F5E5A" stroke-width="1"/>
<line x1="55" y1="100" x2="75" y2="100" stroke="#5F5E5A"/>
<line x1="65" y1="90" x2="65" y2="110" stroke="#5F5E5A"/>
<text x="52" y="85" font-family="sans-serif" font-size="12" fill="#5F5E5A">+</text>
<text x="78" y="125" font-family="sans-serif" font-size="12" fill="#5F5E5A">−</text>
<text x="78" y="93" font-family="sans-serif" font-size="12" fill="#5F5E5A">−</text>

<line x1="79" y1="100" x2="120" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr8)"/>

<rect x="120" y="80" width="60" height="40" rx="6" fill="#EEEDFE" stroke="#534AB7" stroke-width="0.5"/>
<text x="150" y="105" text-anchor="middle" font-family="sans-serif" font-size="12" font-weight="500" fill="#3C3489">К1·Кр·Кп</text>

<line x1="180" y1="100" x2="215" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr8)"/>
<text x="198" y="90" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">Uм</text>

<rect x="215" y="80" width="60" height="40" rx="6" fill="#E1F5EE" stroke="#0F6E56" stroke-width="0.5"/>
<text x="245" y="105" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#085041">М</text>

<line x1="275" y1="100" x2="315" y2="100" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr8)"/>
<text x="295" y="90" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">ω</text>
<circle cx="300" cy="100" r="3" fill="#5F5E5A"/>

<rect x="315" y="80" width="60" height="40" rx="6" fill="#F1EFE8" stroke="#5F5E5A" stroke-width="0.5"/>
<text x="345" y="105" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#2C2C2A">1/p</text>

<line x1="375" y1="100" x2="430" y2="100" stroke="#5F5E5A" stroke-width="2"/>
<text x="410" y="90" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвых</text>

<line x1="425" y1="100" x2="425" y2="260" stroke="#5F5E5A" stroke-width="1.5" stroke-dasharray="4 4"/>
<line x1="425" y1="260" x2="65" y2="260" stroke="#5F5E5A" stroke-width="1.5" stroke-dasharray="4 4"/>
<line x1="65" y1="260" x2="65" y2="114" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr8)"/>
<text x="245" y="275" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">главная ОС по θвых</text>

<line x1="300" y1="100" x2="300" y2="170" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="300" y1="170" x2="440" y2="170" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr8)"/>

<rect x="440" y="150" width="70" height="40" rx="6" fill="#FAEEDA" stroke="#854F0B" stroke-width="0.5"/>
<text x="475" y="175" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#633806">ТГ</text>

<line x1="510" y1="170" x2="540" y2="170" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr8)"/>
<text x="525" y="160" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">Kс·ω</text>

<rect x="540" y="150" width="100" height="40" rx="6" fill="#FAEEDA" stroke="#854F0B" stroke-width="0.5"/>
<text x="590" y="170" text-anchor="middle" font-family="sans-serif" font-size="14" font-weight="500" fill="#633806">RC-цепь</text>
<text x="590" y="185" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#633806">дифф.</text>

<line x1="475" y1="190" x2="475" y2="220" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="475" y1="220" x2="78" y2="220" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="78" y1="220" x2="78" y2="114" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr8)"/>
<text x="275" y="215" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">ОС по 1-й производной: Kс·p·θвых</text>

<line x1="640" y1="170" x2="660" y2="170" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="660" y1="170" x2="660" y2="40" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="660" y1="40" x2="50" y2="40" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="50" y1="40" x2="50" y2="86" stroke="#5F5E5A" stroke-width="1.5" fill="none" marker-end="url(#arr8)"/>
<text x="355" y="33" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">ОС по 2-й производной: Kс·T1·p²·θвых</text>

<text x="20" y="305" font-family="sans-serif" font-size="12" fill="#5F5E5A">ТГ — тахогенератор. RC-цепь дифференцирует сигнал скорости для получения ускорения</text>
</svg>
```

Уравнение напряжения двигателя:

$$U_м = (K_1 \cdot \theta - K_c \cdot p \cdot \theta_{вых}) \cdot K_р \cdot K_п$$

**Результаты анализа:**
- Статическая ошибка θ_ст остаётся прежней
- Скоростная ошибка **увеличивается** в (1 + K_c·K/K₁) раз:

$$\theta_{ск} = \frac{\Omega_{вх}}{K} \cdot \left(1 + \frac{K_c \cdot K}{K_1}\right)$$

- Коэффициент демпфирования колебаний **увеличивается** в (1 + K_c·K/K₁) раз, что позволяет повысить качество переходного процесса даже при большей величине K.

### Обратная связь по второй производной

Для получения обратной связи по второй производной напряжение тахогенератора предварительно **дифференцируют** с помощью дифференцирующей RC-цепочки.

Уравнение напряжения двигателя:

$$U_м = (K_1 \cdot \theta - K_c \cdot T_1 \cdot p^2 \cdot \theta_{вых}) \cdot K_р \cdot K_п$$

**Особенности:**
- Статическая ошибка остаётся неизменной (гибкая обратная связь в статике исчезает)
- Скоростная ошибка не изменяется: θ_ск = Ω_вх/K
- При **отрицательной** обратной связи возрастает инерционность привода:

$$T'_м = T_м + \frac{K \cdot K_c}{K_1} \cdot T_1$$

- При **положительной** обратной связи эквивалентная постоянная времени снижается:

$$T'_м = T_м - \frac{K \cdot K_c}{K_1} \cdot T_1$$

Но при K·K_c/K₁ > T_м коэффициент при p² в характеристическом уравнении становится отрицательным, и **система теряет устойчивость**. Поэтому такой обратной связью следует пользоваться с осторожностью.

---

## 9. Следящий электропривод с пропорционально-дифференциальным законом регулирования

Напряжение U_у на выходе ПД-регулятора имеет две составляющие — пропорциональную сигналу ошибки U_θ и пропорциональную производной сигнала ошибки:

$$U_у = K_р \cdot U_\theta + K_р \cdot \tau \cdot \frac{dU_\theta}{dt} = K_р \cdot (1 + \tau \cdot p) \cdot U_\theta$$

Уравнение напряжения двигателя:

$$U_м = K_1 \cdot K_р \cdot K_п \cdot (1 + \tau \cdot p) \cdot \theta$$

**Итоговое уравнение:**

$$\theta(t) = \frac{T_м \cdot p^2 + p}{T_м \cdot p^2 + (1 + K\tau) \cdot p + K} \cdot \theta_{вх}(t) + \frac{1}{T_м \cdot p^2 + (1 + K\tau) \cdot p + K} \cdot \frac{M_c}{b}$$

**Статическая ошибка:** θ_ст = M_c/(K·b) — такая же, как в предыдущих вариантах.

**Скоростная ошибка:** θ_ск = Ω_вх/K — не изменилась.

**Коэффициент демпфирования** (для характеристического уравнения a₂p² + a₁p + a₀ = 0):

$$x = \frac{a_1}{2\sqrt{a_0 \cdot a_2}} = \frac{1 + K\tau}{2\sqrt{K \cdot T_м}}$$

Для П-регулятора (τ = 0): x = 1/(2√(KT_м)).

**Графики переходных процессов при разных x:**

```svg
<svg width="100%" viewBox="0 0 680 380" xmlns="http://www.w3.org/2000/svg">
<line x1="60" y1="40" x2="60" y2="320" stroke="#5F5E5A" stroke-width="1"/>
<line x1="60" y1="220" x2="640" y2="220" stroke="#5F5E5A" stroke-width="1"/>

<text x="30" y="45" font-family="sans-serif" font-size="12" fill="#5F5E5A">θвых/θвх</text>
<text x="625" y="240" font-family="sans-serif" font-size="12" fill="#5F5E5A">t</text>
<text x="45" y="225" font-family="sans-serif" font-size="12" fill="#5F5E5A">0</text>

<line x1="55" y1="120" x2="60" y2="120" stroke="#5F5E5A"/>
<text x="35" y="125" font-family="sans-serif" font-size="12" fill="#5F5E5A">1,5</text>
<line x1="55" y1="170" x2="60" y2="170" stroke="#5F5E5A"/>
<text x="40" y="175" font-family="sans-serif" font-size="12" fill="#5F5E5A">1</text>
<line x1="60" y1="170" x2="640" y2="170" stroke="#B4B2A9" stroke-width="0.5" stroke-dasharray="3 3"/>

<path d="M60 220 Q90 60 140 120 Q180 260 220 180 Q260 140 300 180 Q340 200 380 170 L620 170" fill="none" stroke="#E24B4A" stroke-width="2"/>
<text x="150" y="80" font-family="sans-serif" font-size="12" fill="#E24B4A">x = 0,3 — колебательный</text>

<path d="M60 220 Q120 130 180 160 Q240 180 300 170 L620 170" fill="none" stroke="#1D9E75" stroke-width="2"/>
<text x="280" y="140" font-family="sans-serif" font-size="12" fill="#0F6E56">x = 0,707 — оптимальный</text>

<path d="M60 220 Q180 190 300 180 Q420 175 540 172 L620 170" fill="none" stroke="#185FA5" stroke-width="2" stroke-dasharray="6 4"/>
<text x="420" y="210" font-family="sans-serif" font-size="12" fill="#0C447C">x = 1,2 — апериодический</text>

<text x="60" y="350" font-family="sans-serif" font-size="12" fill="#5F5E5A">Технически оптимальный переходный процесс: x = √2/2 ≈ 0,707 даёт σ ≤ 5-7%</text>
<text x="60" y="370" font-family="sans-serif" font-size="12" fill="#5F5E5A">при минимальном времени регулирования</text>
</svg>
```

Введение дифференциальной составляющей **увеличивает коэффициент демпфирования в (1 + Kτ) раз**. Это позволяет получить удовлетворительный переходной процесс при значительно большей величине K, а следовательно, при меньших величинах θ_ст и θ_ск.

**Технически оптимальный переходной процесс** (перерегулирование не более 5…7 %) имеет место при коэффициенте демпфирования x = √2/2 ≈ 0,707.

Полагая x = √2/2 оптимальным, определяем необходимую величину параметра τ:

$$\tau_{опт} = \frac{\sqrt{2 \cdot K \cdot T_м} - 1}{K}$$

**Преимущество ПД-регулятора:** позволяет увеличить коэффициент демпфирования без увеличения скоростной составляющей ошибки (в отличие от обратной связи по первой производной).

---

## 10. Выбор исполнительного двигателя для системы управления электроприводом

Выбор исполнительного двигателя для следящего электропривода производится по следующим критериям:

**1. По требуемой мощности и моменту.** Двигатель должен обеспечить заданный момент на валу нагрузки с учётом момента сопротивления М_с и динамического момента J·dω/dt при разгоне.

**2. По максимальной скорости.** Номинальная скорость двигателя (с учётом передаточного числа редуктора) должна соответствовать максимальной требуемой скорости слежения.

**3. По быстродействию.** Важным параметром является электромеханическая постоянная времени T_м = J·R_a/C_E², которая должна быть минимальной для получения высокого быстродействия. Для этого применяют двигатели с малым моментом инерции якоря.

**4. По диапазону регулирования.** Двигатель должен обеспечивать устойчивую работу при малых скоростях без зон нечувствительности.

**5. По характеру нагрузки.** Учитывается частота реверсов, режим работы (продолжительный, повторно-кратковременный).

**Типы применяемых двигателей:**
- Двигатели постоянного тока с независимым возбуждением (классические исполнительные);
- Двигатели постоянного тока с полым якорем или дисковые (малоинерционные);
- Бесколлекторные (вентильные) двигатели постоянного тока (BLDC);
- Шаговые двигатели — для дискретных приводов;
- Асинхронные сервоприводы с частотным управлением.

**Условия проверки:**
- По нагреву (эквивалентный момент не должен превышать номинальный);
- По перегрузочной способности (максимальный момент ≤ допустимый);
- По условию обеспечения требуемого ускорения.

---

## 11. Определение оптимального передаточного числа редуктора

Оптимальное передаточное число редуктора i_опт определяется из условия **минимума момента инерции, приведённого к валу двигателя**, либо из условия **максимума углового ускорения нагрузки**.

**Суммарный момент инерции, приведённый к валу двигателя:**

$$J_\Sigma = J_д + \frac{J_н}{i^2}$$

где J_д — момент инерции ротора двигателя, J_н — момент инерции нагрузки, i — передаточное число редуктора.

**Приведённый момент сопротивления:**

$$M_{с.пр} = \frac{M_с}{i \cdot \eta}$$

где η — КПД редуктора.

**График зависимости J_Σ от i:**

```svg
<svg width="100%" viewBox="0 0 680 360" xmlns="http://www.w3.org/2000/svg">
<line x1="60" y1="40" x2="60" y2="300" stroke="#5F5E5A" stroke-width="1"/>
<line x1="60" y1="300" x2="640" y2="300" stroke="#5F5E5A" stroke-width="1"/>

<text x="30" y="45" font-family="sans-serif" font-size="12" fill="#5F5E5A">JΣ</text>
<text x="620" y="320" font-family="sans-serif" font-size="12" fill="#5F5E5A">i</text>
<text x="45" y="305" font-family="sans-serif" font-size="12" fill="#5F5E5A">0</text>

<line x1="60" y1="230" x2="640" y2="230" stroke="#185FA5" stroke-width="1.5" stroke-dasharray="4 4"/>
<text x="580" y="220" font-family="sans-serif" font-size="12" fill="#0C447C">Jд = const</text>

<path d="M80 60 Q100 120 130 180 Q170 230 240 260 Q320 275 420 282 Q520 288 620 292" fill="none" stroke="#993C1D" stroke-width="1.5" stroke-dasharray="4 4"/>
<text x="120" y="110" font-family="sans-serif" font-size="12" fill="#712B13">Jн/i²</text>

<path d="M80 55 Q100 100 140 135 Q200 175 280 200 Q360 215 440 220 Q520 225 620 230" fill="none" stroke="#0F6E56" stroke-width="2.5"/>
<text x="300" y="170" font-family="sans-serif" font-size="12" fill="#0F6E56">JΣ = Jд + Jн/i²</text>

<line x1="250" y1="40" x2="250" y2="300" stroke="#E24B4A" stroke-width="1.5" stroke-dasharray="6 4"/>
<text x="260" y="55" font-family="sans-serif" font-size="12" font-weight="500" fill="#A32D2D">i_опт = √(Jн/Jд)</text>
<circle cx="250" cy="190" r="4" fill="#E24B4A"/>

<text x="60" y="335" font-family="sans-serif" font-size="12" fill="#5F5E5A">Минимум JΣ достигается при i_опт = √(Jн/Jд) — приведённая Jн равна Jд</text>
</svg>
```

**Условие оптимальности** (из условия максимального ускорения нагрузки при заданном моменте двигателя):

$$i_{опт} = \sqrt{\frac{J_н}{J_д}}$$

При этом приведённый к валу двигателя момент инерции нагрузки равен моменту инерции самого двигателя (J_н/i² = J_д), и обеспечивается наилучшее согласование инерционностей ("принцип равенства моментов инерции").

**Для случая с учётом момента сопротивления** оптимальное передаточное число определяется из условия минимума времени разгона:

$$i_{опт} = \frac{M_с}{M_д} + \sqrt{\left(\frac{M_с}{M_д}\right)^2 + \frac{J_н}{J_д}}$$

где M_д — номинальный момент двигателя.

При выбранном i_опт проверяется соответствие номинальной скорости двигателя требуемой максимальной скорости нагрузки: ω_д.ном ≥ i·ω_н.max.

---

## 12. Выбор измерителя рассогласования для системы управления электроприводом

Измеритель рассогласования — устройство, преобразующее разность между заданным и действительным положением выходного вала в электрический сигнал.

**Основные типы:**

**1. Сельсинная пара (сельсин-датчик и сельсин-приёмник в трансформаторной схеме)** — применяется в следящих электроприводах с непрерывным управлением. Ротор СД соединён с задающим валом, ротор СП — с выходным валом. Выходное напряжение U_θ = U_m·sin θ, фаза зависит от знака угла рассогласования.

**2. Потенциометрическая пара (П1 и П2)** — применяется в релейных и импульсных следящих электроприводах. Разность напряжений U_θ = U_вх − U_вых пропорциональна углу рассогласования.

**3. Вращающиеся трансформаторы (ВТ)** — применяются для прецизионных измерений с высокой точностью.

**4. Цифровые датчики угла** — оптические (фотоимпульсные) энкодеры, кодовые диски — для цифровых систем управления.

**5. Индуктосины, резольверы** — для прецизионных систем.

**Критерии выбора измерителя рассогласования:**

- **Требуемая точность** — для высокоточных систем применяют ВТ, индуктосины, цифровые энкодеры высокого разрешения;
- **Диапазон измеряемых углов** — однооборотные или многооборотные датчики;
- **Быстродействие** — важна полоса пропускания датчика;
- **Тип системы управления** — аналоговая (сельсины, ВТ, потенциометры) или цифровая (энкодеры, кодовые диски);
- **Условия эксплуатации** — температура, вибрации, влажность;
- **Стоимость и надёжность** — потенциометры дёшевы, но менее надёжны; сельсины и ВТ имеют бо́льший ресурс;
- **Наличие электрических шумов и помех** — бесконтактные датчики (ВТ, энкодеры) предпочтительнее.

---

## 13. Оценка качества следящей системы по виду ЛАЧХ разомкнутой системы

**Логарифмическая амплитудно-частотная характеристика (ЛАЧХ)** разомкнутой системы L(ω) = 20·lg|W(jω)| — один из важнейших инструментов оценки качества следящих систем.

**Желаемая ЛАЧХ разомкнутой следящей системы:**

```svg
<svg width="100%" viewBox="0 0 680 420" xmlns="http://www.w3.org/2000/svg">
<line x1="60" y1="50" x2="60" y2="340" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="60" y1="210" x2="640" y2="210" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="640" y1="210" x2="645" y2="205" stroke="#5F5E5A" stroke-width="1.5"/>
<line x1="640" y1="210" x2="645" y2="215" stroke="#5F5E5A" stroke-width="1.5"/>

<text x="30" y="50" font-family="sans-serif" font-size="14" font-weight="500" fill="#2C2C2A">L, дБ</text>
<text x="620" y="230" font-family="sans-serif" font-size="14" font-weight="500" fill="#2C2C2A">lg ω</text>
<text x="50" y="215" font-family="sans-serif" font-size="12" fill="#5F5E5A">0</text>

<line x1="55" y1="110" x2="60" y2="110" stroke="#5F5E5A"/>
<text x="30" y="115" font-family="sans-serif" font-size="12" fill="#5F5E5A">40</text>
<line x1="55" y1="160" x2="60" y2="160" stroke="#5F5E5A"/>
<text x="30" y="165" font-family="sans-serif" font-size="12" fill="#5F5E5A">20</text>
<line x1="55" y1="260" x2="60" y2="260" stroke="#5F5E5A"/>
<text x="25" y="265" font-family="sans-serif" font-size="12" fill="#5F5E5A">−20</text>

<line x1="150" y1="50" x2="150" y2="340" stroke="#B4B2A9" stroke-width="0.5" stroke-dasharray="3 3"/>
<line x1="310" y1="50" x2="310" y2="340" stroke="#B4B2A9" stroke-width="0.5" stroke-dasharray="3 3"/>
<line x1="400" y1="50" x2="400" y2="340" stroke="#B4B2A9" stroke-width="0.5" stroke-dasharray="3 3"/>
<line x1="510" y1="50" x2="510" y2="340" stroke="#B4B2A9" stroke-width="0.5" stroke-dasharray="3 3"/>

<polyline points="80,80 150,130 310,210 400,210 510,290 600,350" fill="none" stroke="#185FA5" stroke-width="2.5"/>

<text x="95" y="95" font-family="sans-serif" font-size="12" fill="#185FA5">−20 дБ/дек</text>
<text x="195" y="155" font-family="sans-serif" font-size="12" fill="#185FA5">−20 дБ/дек</text>
<text x="330" y="200" font-family="sans-serif" font-size="12" fill="#185FA5">−20 дБ/дек</text>
<text x="430" y="245" font-family="sans-serif" font-size="12" fill="#185FA5">−40 дБ/дек</text>
<text x="540" y="320" font-family="sans-serif" font-size="12" fill="#185FA5">−60 дБ/дек</text>

<text x="150" y="360" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">ω1</text>
<text x="310" y="360" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">ω2</text>
<text x="355" y="360" text-anchor="middle" font-family="sans-serif" font-size="12" font-weight="500" fill="#993C1D">ωср</text>
<text x="400" y="360" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">ω3</text>
<text x="510" y="360" text-anchor="middle" font-family="sans-serif" font-size="12" fill="#5F5E5A">ω4</text>

<circle cx="355" cy="210" r="5" fill="#993C1D"/>

<rect x="60" y="50" width="250" height="8" fill="#AFA9EC" opacity="0.5"/>
<text x="185" y="45" text-anchor="middle" font-family="sans-serif" font-size="12" font-weight="500" fill="#3C3489">Низкочастотная — точность</text>

<rect x="310" y="50" width="90" height="8" fill="#5DCAA5" opacity="0.6"/>
<text x="355" y="45" text-anchor="middle" font-family="sans-serif" font-size="12" font-weight="500" fill="#085041">Среднечастотная</text>

<rect x="400" y="50" width="240" height="8" fill="#F0997B" opacity="0.5"/>
<text x="520" y="45" text-anchor="middle" font-family="sans-serif" font-size="12" font-weight="500" fill="#712B13">Высокочастотная — помехи</text>

<text x="60" y="390" font-family="sans-serif" font-size="12" fill="#5F5E5A">НЧ: высокий уровень ЛАЧХ → малые θст, θск. Наклон −20 дБ/дек = астатизм 1-го порядка</text>
<text x="60" y="410" font-family="sans-serif" font-size="12" fill="#5F5E5A">СЧ: наклон −20 дБ/дек в окрестности ωср, протяжённость ≥ 1 декады</text>
</svg>
```

### Структура ЛАЧХ

Типовая ЛАЧХ следящего электропривода содержит три характерные области:

**1. Низкочастотная область** — определяет **точность системы в установившихся режимах**.
- Наклон −20 дБ/дек соответствует астатизму 1-го порядка (статическая ошибка отсутствует при постоянном задании);
- Наклон −40 дБ/дек — астатизму 2-го порядка (и скоростная ошибка равна нулю);
- Чем выше коэффициент усиления K (выше ЛАЧХ в НЧ-области), тем меньше ошибки θ_ст и θ_ск.

**2. Среднечастотная область** — определяет **качество переходного процесса** (устойчивость, запасы устойчивости, перерегулирование).
- Наклон в области частоты среза ω_ср должен составлять **−20 дБ/дек**;
- Протяжённость участка с наклоном −20 дБ/дек должна быть не менее 1 декады (желательно симметрично относительно ω_ср);
- Частота среза ω_ср определяет **быстродействие системы**: время регулирования t_р ≈ (1…2)·2π/ω_ср.

**3. Высокочастотная область** — определяет **помехозащищённость системы**. Желательны большие наклоны (−40, −60 дБ/дек) для подавления высокочастотных помех.

### Показатели качества по ЛАЧХ

**Запас устойчивости по амплитуде** ΔL — расстояние по вертикали от оси 0 дБ до точки ЛАЧХ на частоте, где фаза равна −180°. Норма: ΔL ≥ 10…12 дБ.

**Запас устойчивости по фазе** Δφ — разность между −180° и значением фазы на частоте среза ω_ср. Норма: Δφ ≥ 30…60°.

**Частота среза** ω_ср — частота, на которой L(ω_ср) = 0. Определяет полосу пропускания замкнутой системы и быстродействие.

**Связь с перерегулированием:**
- При наклоне −20 дБ/дек в области среза и Δφ ≈ 60° — перерегулирование σ ≈ 20…30%;
- При Δφ ≈ 45° — σ ≈ 40%;
- При Δφ ≈ 30° — σ > 50% (неудовлетворительное качество).

### Методика оценки

1. Построить ЛАЧХ разомкнутой системы.
2. По низкочастотной части оценить статическую и скоростную ошибки (чем выше ЛАЧХ, тем меньше ошибки).
3. По среднечастотной части оценить устойчивость и быстродействие (наклон в области ω_ср должен быть −20 дБ/дек).
4. Проверить запасы устойчивости по амплитуде и фазе.
5. По высокочастотной части оценить помехозащищённость.

**Желаемая ("оптимальная") ЛАЧХ** для следящих систем строится так, чтобы обеспечить:
- высокую точность (большой K в НЧ-области);
- удовлетворительные переходные процессы (наклон −20 дБ/дек в районе ω_ср);
- защиту от помех (большие наклоны в ВЧ-области).

Сравнение реальной ЛАЧХ системы с желаемой позволяет определить, какие корректирующие звенья (последовательные или параллельные) необходимо ввести в систему для улучшения её качества.

---

## Приложение. Сравнительная таблица вариантов следящих электроприводов

| № | Вариант | θ_ст | θ_ск | Демпф. x | Ключевая идея |
|---|---------|------|------|----------|---------------|
| 1 | П-регулятор, ОС по θ | M_с/(Kb) | Ω_вх/K | x₀ | Базовый: ↑K душит точность, но раскачивает |
| 2 | + ОС по ω (тахогенератор) | = 1 | ↑ в α раз | ↑ в α раз | Гасит колебания ценой скоростной ошибки |
| 3 | + ОС по a (положит.) | = 1 | = 1 | ↑ | Снижает T_м, но есть риск потери устойчивости |
| 4 | **ПД-регулятор** ⭐ | = 1 | = 1 | **↑ в (1+Kτ)** | **Демпфирование без роста θ_ск** |
| 5 | ПИ-регулятор | **= 0** | **= 0** | — | Астатическая система. Порядок ур-я ↑ до 3-го |
| 6 | + коррекция по M_с | ↓ или =0 | Ω_вх/K | x₀ | Комбинированное: компенсирует возмущение |

где α = (1 + K_c·K/K₁).

**Три ключевых вывода:**
1. Увеличение K снижает ошибки, но ухудшает переходный процесс — всегда компромисс.
2. ПД лучше ОС по скорости (не растёт θ_ск), ПИ убирает ошибки полностью.
3. Коррекция по возмущению — независимый инструмент.
