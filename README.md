# Анкета на вакансию Специалист по разметке данных со знанием разработки

1. Выбрать все элементы ВВВ, имеющие трех предков.
```xml
<AAA> 
  <XXX> 
     <DDD> 
        <BBB></BBB> 
        <BBB></BBB> 
        <EEE></EEE> 
        <FFF></FFF> 
     </DDD> 
  </XXX> 
  <CCC> 
     <DDD> 
        <BBB></BBB> 
        <BBB></BBB> 
        <EEE></EEE> 
        <FFF></FFF> 
     </DDD> 
   </CCC> 
   <CCC> 
      <BBB> 
        <BBB> 
          <BBB></BBB> 
        </BBB> 
      </BBB> 
   </CCC> 
 </AAA>
```
- [ ] //BBB[3]
- [x] //\*/\*/*/BBB
- [ ] //\*/\*/*/BBB[3]
- [ ] //BBB[count(./ancestor::*)=3]
- [ ] нет правильного варианта

2. Выберите второго потомка ВВВ элемента ААА.
```xml
<AAA> 
     <BBB></BBB> 
     <BBB></BBB> 
     <BBB></BBB> 
     <BBB></BBB> 
</AAA>
```
- [ ] //AAA/BBB/BBB
- [x] //AAA/BBB[2]
- [ ] //AAA/*/BBB
- [ ] //AAA[2]/BBB
- [ ] нет правильного варианта

3. Выберите элементы BBB, не имеющие ни одного атрибута.
```xml
<AAA> 
     <BBB id = "b1"></BBB> 
     <BBB id = "b2"></BBB> 
     <BBB name = "bbb"></BBB> 
     <BBB></BBB> 
</AAA>
```
- [x] //BBB[not(@*)]
- [x] //BBB[count(./attribute::*)=0]
- [ ] //BBB[not(@='')]
- [ ] //BBB[not(@id)]
- [ ] нет правильного варианта

4. Выберите все элементы, имя которых содержит C.
```xml
<AAA> 
    <BCC> 
         <BBB></BBB> 
         <BBB></BBB> 
         <BBB></BBB> 
    </BCC> 
    <DDB> 
         <BBB></BBB> 
         <BBB></BBB> 
    </DDB> 
    <BEC> 
         <CCC></CCC> 
         <DBD></DBD> 
    </BEC> 
</AAA>
```
- [ ] //*/name()[contains('C')]
- [x] //*[contains(name(),'C')]
- [x] //*[contains(name(.),'C')]
- [ ] //name()[contains('C')]
- [ ] нет правильного варианта

5. Выберите все элементы, имя которых состоит более чем из трех символов.
```xml
<AAA> 
      <Q></Q> 
      <SSSS></SSSS> 
      <BB></BB> 
      <CCC></CCC> 
      <DDDDDDDD></DDDDDDDD> 
      <EEEE></EEEE> 
 </AAA>
```
- [x] //*[string-length(name()) > 3]
- [x] //*[string-length(name(.))>3]
- [ ] //*[position()(name()) > 3]
- [ ] //*[length(name()) > 3]
- [ ] нет правильного варианта

6. Напишите Xpath до элемента, содержащего текст "Сообщение 1".
```html
<input type="checkbox">
<input type="checkbox" checked>
<input type="text" id="message">

<h3 id="widget-title">Сообщения:</h3>
<ul id="messages">
    <li id="message-1">Сообщение 1</li>
    <li id="message-2">Сообщение 2</li>
    <li id="message-3" data-action="delete">Сообщение 3</li>
    <li id="message-4" data-action="edit do-not-delete">Сообщение 4</li>
    <li id="message-5" data-action="edit delete">Сообщение 5</li>
    <li><a href="#">...</a></li>
</ul>

<a href="http://site.com/list.zip">Ссылка на архив</a>
<a href="http://site.com/list.pdf">..И на PDF</a>
```
- [ ] //UL[@id='messages']/LI[contains(.,'Сообщение 1')]/LI[1]
- [x] //UL[@id='messages']/LI[contains(.,'Сообщение 1')]
- [ ] //*[contains(./text(),'Сообщение 1')]
- [ ] //H3/UL[@id='messages']/LI[contains(.,'Сообщение 1')]
- [ ] нет правильного варианта
 
6. Напишите Xpath до элемента, содержащего текст "Сообщение 1".
```html
<input type="checkbox">
<input type="checkbox" checked>
<input type="text" id="message">

<h3 id="widget-title">Сообщения:</h3>
<ul id="messages">
    <li id="message-1">Сообщение 1</li>
    <li id="message-2">Сообщение 2</li>
    <li id="message-3" data-action="delete">Сообщение 3</li>
    <li id="message-4" data-action="edit do-not-delete">Сообщение 4</li>
    <li id="message-5" data-action="edit delete">Сообщение 5</li>
    <li><a href="#">...</a></li>
</ul>

<a href="http://site.com/list.zip">Ссылка на архив</a>
<a href="http://site.com/list.pdf">..И на PDF</a>
```
- [ ]
- [ ]
- [ ]
- [ ]
- [ ]

6. Напишите Xpath до элемента, содержащего текст "Сообщение 1".
```html
<input type="checkbox">
<input type="checkbox" checked>
<input type="text" id="message">

<h3 id="widget-title">Сообщения:</h3>
<ul id="messages">
    <li id="message-1">Сообщение 1</li>
    <li id="message-2">Сообщение 2</li>
    <li id="message-3" data-action="delete">Сообщение 3</li>
    <li id="message-4" data-action="edit do-not-delete">Сообщение 4</li>
    <li id="message-5" data-action="edit delete">Сообщение 5</li>
    <li><a href="#">...</a></li>
</ul>

<a href="http://site.com/list.zip">Ссылка на архив</a>
<a href="http://site.com/list.pdf">..И на PDF</a>
```
- [ ]
- [ ]
- [ ]
- [ ]
- [ ]

6. Напишите Xpath до элемента, содержащего текст "Сообщение 1".
```html
<input type="checkbox">
<input type="checkbox" checked>
<input type="text" id="message">

<h3 id="widget-title">Сообщения:</h3>
<ul id="messages">
    <li id="message-1">Сообщение 1</li>
    <li id="message-2">Сообщение 2</li>
    <li id="message-3" data-action="delete">Сообщение 3</li>
    <li id="message-4" data-action="edit do-not-delete">Сообщение 4</li>
    <li id="message-5" data-action="edit delete">Сообщение 5</li>
    <li><a href="#">...</a></li>
</ul>

<a href="http://site.com/list.zip">Ссылка на архив</a>
<a href="http://site.com/list.pdf">..И на PDF</a>
```
- [ ]
- [ ]
- [ ]
- [ ]
- [ ]

6. Напишите Xpath до элемента, содержащего текст "Сообщение 1".
```html
<input type="checkbox">
<input type="checkbox" checked>
<input type="text" id="message">

<h3 id="widget-title">Сообщения:</h3>
<ul id="messages">
    <li id="message-1">Сообщение 1</li>
    <li id="message-2">Сообщение 2</li>
    <li id="message-3" data-action="delete">Сообщение 3</li>
    <li id="message-4" data-action="edit do-not-delete">Сообщение 4</li>
    <li id="message-5" data-action="edit delete">Сообщение 5</li>
    <li><a href="#">...</a></li>
</ul>

<a href="http://site.com/list.zip">Ссылка на архив</a>
<a href="http://site.com/list.pdf">..И на PDF</a>
```
- [ ]
- [ ]
- [ ]
- [ ]
- [ ]
 































































