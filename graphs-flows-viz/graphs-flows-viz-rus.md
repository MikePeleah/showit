# Визуализация графов, сетей и потоков 
Версия 2.3, 28 мая 2024. Собрано [Mike Peleah](https://www.linkedin.com/in/peleah/). [![CC BY-NC-SA 4.0](CC_BY-NC-SA_4.0_30px.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/). Комментарии автору можно отправить на [емэйл](mailto:mike.peleah@gmail.com?subject=Визуализация графов, сетей и потоков) или в Телеграм [@voodoo_woodpecker](https://t.me/voodoo_woodpecker)


Графы и сети окружают нас повсюду, и многие вещи находятся в постоянном движении, что можно наглядно продемонстрировать через динамическую визуализацию. Например, социальные сети отображают взаимоотношения и коммуникации между людьми, где каждый узел представляет человека, а связи между узлами — их взаимодействия. В транспортных системах графы используются для моделирования движения поездов, самолетов и автомобилей, где узлы — это станции или аэропорты, а ребра — маршруты. В биологических системах графы помогают исследовать сети взаимодействий между генами, белками и клетками. Динамические визуализации этих графов могут показывать изменение связей и потоков в реальном времени, что позволяет лучше понять, анализировать и предсказывать поведение систем.


# Графы и сети
## Когда графы были маленькими
Графы и сети имеют [долгую историю](https://ru.wikipedia.org/wiki/%D0%A2%D0%B5%D0%BE%D1%80%D0%B8%D1%8F_%D0%B3%D1%80%D0%B0%D1%84%D0%BE%D0%B2). До 18 века они в основном использовались в виде деревьев, например генеаологических деревьев. В их визуализации преобладала эстетическая фцнкция, а число узлов и связей было незначительным. В 18-19 века графы начали активно использоваться в качестве удобного математического аппарата, например для [задачи о семи кёнигсбергских мостах](https://ru.wikipedia.org/wiki/%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0_%D0%BE_%D1%81%D0%B5%D0%BC%D0%B8_%D0%BA%D1%91%D0%BD%D0%B8%D0%B3%D1%81%D0%B1%D0%B5%D1%80%D0%B3%D1%81%D0%BA%D0%B8%D1%85_%D0%BC%D0%BE%D1%81%D1%82%D0%B0%D1%85), анализа электрических цепей, органических молекул, и многих других задач. Число узлов и связей оставалось незначительным. Для визуализации графов использовались схематичные изображения вершин и связей между ними, дополнительные параметры редко визуализировались. 

![Родословное дерево русских государей, 1731](Genealogical_Tree_Russian_Tzars.png)

[Никитин И. Н. Родословное дерево русских государей, 1731. Коллекция Государственного Русского музея](https://rusmuseumvrm.ru/data/collections/painting/17_19/nikitin_i_rodoslovnoe_derevo_russkih_gosudarey_1731_zh_3/index.php)


## Internets come to town
Интернет начинался в 1969 году с трёх узлов в Университах UCLA и Stanford, но начал очень быстро расти. Если в 1970-х годах схемы интернета ещё умещались на лист бумаги, то [в 2011 году карта интернета](http://internet-map.net/) была похоже на карту галактики — залипательную, но непрактичную. Для визуализации сетей было важно показать взаимосвязи (физические) между узлами и тип узла (используемое оборудование). От этих параметров зависело движение пакетов и пропускная способность узлов — идея была в обеспечении гарантированной передачи пакетов даже при повреждении значительного числа узлов. Так как визуализация всего Интернета стала достаточно непрактичной, подход сдвинулся в сторону визуализации фрагментов сети. В этом случае детально визуализируется только часть, например находящаяся в области ответственности администратора или связанная непосредственно с данным узлом (например, в рутерах). В таком случае указываются узлы, их типы (чаще всего визуализируются стандартными иконками). Такие визцализации могут быть интерактивными и предсотавлять дополнительную информацию (IP адрес, статус, доступ к настройкам доступа и др.)

![A sketch of the ARPANET in December 1969](A_sketch_of_the_ARPANET_in_December_1969.png)

[A sketch of the ARPANET in December 1969. The nodes at UCLA and the Stanford Research Institute (SRI) are among those depicted. Wikimedia Commons](https://en.wikipedia.org/wiki/File:A_sketch_of_the_ARPANET_in_December_1969.png)


![Arpanet map 1973](Arpanet_map_1973.jpg)

[Map of the ARPANET 1973. Wikimedia Commons](https://en.wikipedia.org/wiki/File:Arpanet_map_1973.jpg)


![Arpanet logical map, march 1977](Arpanet_logical_map,_march_1977.png)

[ARPANET logical map circa 1977. Wikimedia Commons](https://en.wikipedia.org/wiki/File:Arpanet_logical_map,_march_1977.png)


![Illustration of a network topology with wireless and mobile devices where some devices are infected with malware or hacking](Illustration-of-a-network-topology.jpg)

[El-Alfy, El-Sayed & Al-Obeidat, Feras. (2015). Detecting Cyber-Attacks on Wireless Mobile Networks Using Multicriterion Fuzzy Classifier with Genetic Attribute Selection. Mobile Information Systems. 2015. 1-13. 10.1155/2015/585432.](https://www.researchgate.net/publication/282772151_Detecting_Cyber-Attacks_on_Wireless_Mobile_Networks_Using_Multicriterion_Fuzzy_Classifier_with_Genetic_Attribute_Selection)


## Социальные сети 
В начале 2000 годов начался бум исследований в области социальных сетей. 
Статья 2002 года рассматривала образование сообществ на примере клуба карате ([старое исследование 1970-х годов](https://en.m.wikipedia.org/wiki/Zachary%27s_karate_club)) и сетей коллаборации в Santa Fe Institute. Если в случае клуба карате количество узлов было всего лишь 34, то в других случаях — сети коллаборации в университетах или графы дружбы в Facebook — количество узлов (и связей между ними) быстро росло, достигая сотен и даже тысяч. Визуализации стали очень сложными, превращаясь в огромные облака, красивые но не сильно практичные. Выходом стали алгоритмы, которые позволяли группировать узлы в сообщества или выделять наиболее важные узлы по количеству связей. Обработанные таким образом сети уже легче визуализировать — показывать сообщества, выделять фрагменты для подробной визуализации и др.


[Girvan, M., & Newman, M. E. (2002). Community structure in social and biological networks. Proceedings of the National Academy of Sciences of the United States of America, 99(12), 7821–7826](https://doi.org/10.1073/pnas.122653799)


![Zachary karate club](Zachary_karate_club.png)

[(a) The friendship network from Zachary's karate club study. Nodes associated with the club administrator's faction are drawn as circles, those associated with the instructor's faction are drawn as squares. (b) Hierarchical tree showing the complete community structure for the network calculated by using the algorithm](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC122977/)


![Santa Fe Institute collaboration network](Santa_Fe_Institute_collaboration_network.jpg)

[The largest component of the Santa Fe Institute collaboration network, with the primary divisions detected by algorithm indicated by different vertex shapes](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC122977/)


## Библиография 
Хороший пример визуализации представляет [ConnectedPapers](https://www.connectedpapers.com/). Он эффективно отображает часть сети научных статей вокруг выбранной статьи, обеспечивая высокую читаемость и информативность. Эта насыщенная данными диаграмма удачно балансирует объем информации и удобство восприятия. Важность статей в сети обозначается размером кружка, основанным на количестве цитирований. Цветовое кодирование используется для отображения времени публикации, что позволяет легко различать новые и старые работы. Интерактивность визуализации позволяет пользователям получать дополнительную информацию при выделении отдельных элементов, что делает исследование более глубоким и детализированным. Визуализация является гибкой, ConnectedPapers позволяет представлять одну и ту же информацию в различных форматах — таблицы или графы — что обеспечивает удобство для пользователей с разными потребностями и предпочтениями.  


![Визуализация статьи Science mapping software tools: Review, analysis, and cooperative study among tools](connected_papers_0b4c513b66754d5e7c700508629e2d28b1061609.png)

[ConnectedPapers](https://www.connectedpapers.com/main/0b4c513b66754d5e7c700508629e2d28b1061609/graph?utm_source=share_popup&utm_medium=copy_link&utm_campaign=share_graph)


Для сравнения большой граф цитирования Web of Science, визуализация Dávid Deritei & Levente Varga (2015 edition)
![Citation networks in the Web of Science by Dávid Deritei & Levente Varga (2015 edition)](Citation_Network_Web_of_Science_DNS.jpg)

[CEU Department of Network & Data Science, twwet Jan 8, 2018](https://x.com/dnds_ceu/status/950390387834785792)


## Торговля
Пространство продуктов (Product Space) представляет собой сеть, соединяющую продукты на основании вероятности совместного экспортировата. Эту сеть можно использовать для прогнозирования будущего экспорта, поскольку страны с большей вероятностью начнут экспортировать продукцию, связанную с текущим экспортом. В такой диаграмме размер узлов соответствует объёму экспорта, цвета — товарной группе, подсвечиваются товары имеющие конкурентное преимущество (RCA, Revealed Comparative Advantage). Детали методологиии в статье [Hidalgo, C. A. & Hausmann, R. The building blocks of economic complexity. Proc. Natl Acad. Sci. USA 106, 10570–10575 (2009)](https://doi.org/10.1073/pnas.0900943106)

![Product Space China, 2022](Product_Space_CHN_2022.png)

[Observatory of Economic Compelxity, Product Space China, 2022](https://oec.world/en/profile/country/chn)

# Потоки 
Наиболее часто используемым инструментом для визуализации является [диаграмма Сэнкей (Sankey diagram)](https://en.wikipedia.org/wiki/Sankey_diagram), изначально придуманная в 1898 году для демонстрации энергоэффективности парового двигателя. В этом случае элементы графа постоянны, а упор делается на визуализацию потоков между ними и характеристики этих потоков, например объём, мощность. 

## Материальные потоки
Евростат использует диаграмму Сэнкей для визуализации материальных потоков в Европейском Союзе 

![Eurostat Material Flows](Eurostat_Material_Flows.png)

[Material Flows, European Union - year 2022](https://ec.europa.eu/eurostat/cache/sankey/circular_economy/sankey.html)


## Метаболизм городов 
Визуализация метаболизма городов с помощью диаграмм Сэнкей позволяет наглядно отображать и анализировать потоки ресурсов, энергии и отходов, что способствует лучшему пониманию и может помогать в оптимизации устойчивости и эффективности городских систем — например, выявляя утечки и потери эффектвиности. Диаграммы Санкея важны, потому что они демонстрируют, как ресурсы перемещаются через различные элементы городской инфраструктуры, выявляя узкие места и возможности для улучшения. В этих диаграммах потоки (стрелки) отображают количество и направление перемещающихся ресурсов, энергии или отходов, которые могут изменяться в зависимости от времени и условий, в то время как узлы (основные элементы системы, такие как заводы, жилые здания или транспортные узлы) остаются относительно постоянными, обеспечивая основу для анализа и интерпретации данных.

![Vancouver B.C. MetaFlow Diagrams for energy (left) and food (right). Credit: Dr. Philip Mansfield/Graphical Memes](MetaFlow_Vancouver.jpeg)

[Urban Metabolism: A Real World Model for Visualizing and Co-Creating Healthy Cities](https://www.thenatureofcities.com/2018/07/24/urban-metabolism-real-world-model-visualizing-co-creating-healthy-cities/)


# Вопросы для визуализации 
- Насколько большую систему я визуализирую? 
- Нужна ли мне вся информация сразу? Могу ли я её упростить? Например, показать только фрагмент системы? Или аггрегировать некоторые параметры?
- Что мне важно показать? Узлы? Типы узлов? Связи между ними? Направленные или ненаправленные связи? Имеет ли значение объём потоков?
- Что статично, а что динамично? Например, меняются ли сами узлы? Свзязи между узлами?


# Инструменты 
## Самостоятельные пакеты
[Gephi](https://gephi.org/) — это мощный и удобный инструмент, "типа как Фотошоп, но для графов", как пишут сами авторы. Пакет с открытым исходным кодом для визуализации и анализа сложных сетей и графов, который позволяет исследователям и аналитикам эффективно представлять и интерпретировать данные. Из минусов — полученные визцализации не очень интерактивны и пакет иногда чудит. 
[Kumu](https://kumu.io/) — гибкий инструмент для визуализации и анализа сетейи графов. Позволяет  пользователям создавать интерактивные карты сложных систем и отношений. Даёт возможность выбора из нескольких шаблонов — визуализация сетей, систем, динамическая или статическая. Фишка — украшательство на основании данных, что позовляет создавать интерактивные диаграммы и разнообразные диаграммы на основании одного набора данных. Умеет брать данные из Google.Sheet, что позволяет раздалить "код" и "данные" диаграммы 👨‍💻 Требует оплаты за приватные проекты. Так как написан на JS, начинает медленно работать на 250+ узлов для интерактивной диаграммы. 
[cytoscape](https://cytoscape.org/) — это мощный и расширяемый инструмент с открытым исходным кодом для визуализации и анализа сложных сетей, особенно биологических, предлагающий богатый функционал и интеграцию с множеством плагинов, но может требовать значительных вычислительных ресурсов и иметь более сложный интерфейс для начинающих пользователей. Имеет возможность програмирования на JS 👨‍💻, см. [cytoscape.js](https://js.cytoscape.org/). [В PubMed Central](https://www.ncbi.nlm.nih.gov/pmc/?term=(cytoscape+AND+network)&report=imagesdocsum&dispmax=100) можно найти много примеров визуализации на cytoscape


## Пакеты для Python
[Plotly](https://plotly.com//) умеет рисовать и [сети](https://plotly.com/python/network-graphs/) и [диаграмма Сэнкей](https://plotly.com/python/sankey-diagram/)
[cytoscape.js](https://js.cytoscape.org/) — это мощная библиотека JavaScript для визуализации и анализа графов в веб-приложениях, предлагающая высокую производительность и гибкость настройки, однако может потребовать значительных усилий на начальную настройку и интеграцию в сложные проекты. Есть адаптация для R, [RCyjs](https://www.bioconductor.org/packages/release/bioc/html/RCyjs.html)






