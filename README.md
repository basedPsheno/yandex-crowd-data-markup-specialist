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




























































