<h1>Актуальность</h1>
Ниже представлено мое семантическое аннотирование библеотеки MicroPather написаной leethomason на С++. Я надеюсь это поможет разобраться в используемых приемах всем желающим.
<br>
Below is my semantic annotation of the MicroPather library written by leethomason in C++. I hope this will help everyone understand the techniques used.
<br>
https://github.com/leethomason/MicroPather
<p>
<p>
<h2><strong>1.Описание библеотеки</strong></h2>
<br>
MicroPather решает задачи по поиску путей, в том числе A* (astar или a-star), написан независимо от платформы C++, который может быть легко интегрирован в существующий код. MicroPather фокусируется на том, чтобы быть механизмом поиска путей для видеоигр, но является универсальным решателем A *. MicroPather имеет открытый исходный код с лицензией, подходящей для использования с открытым исходным кодом или в коммерческих целях. 
<p>Целями MicroPather являются: 
<p>
&emsp;•	Простая интеграция в игры и другое программное обеспечение. 
<p>
&emsp;•	Простой в использовании и понятный интерфейс. 
<p>
&emsp;•	Быстродействие
<p>
<h2><strong>2. Описание темы	</strong></h2>
<br>
В видеоиграх проблема поиска пути возникает во многих современных играх. Каково кратчайшее расстояние от точки А до точки В? Люди хорошо справляются с этой проблемой. Вы естественным образом находите путь почти каждый раз, когда двигаетесь, но его сложно выразить в виде компьютерного алгоритма. A * - это метод "рабочей лошадки" для решения путевых задач. Он оптимизирован для быстрого поиска решения, а не с помощью грубой силы, но он никогда не подведет, если решение есть.<p>
A * гораздо более универсален, чем просто поиск пути. A * и MicroPather можно было бы использовать для поиска решения задач общего состояния, например, их можно было бы использовать для решения головоломки с кубиком рубика.
<p>
<h2><strong>3. Описание процесса установки библиотеки </strong></h2>
<br>
Вкратце, эти шаги таковы:
1.	Включите файлы MicroPather 
2.	Реализуйте графический интерфейс
3.	Вызовите решателя
4.	Включите файлы программы
Есть только 2 файла для micropather: micropather.cpp и micropather.h. Таким образом, нет ни сборки, ни make, просто добавьте эти 2 файла в свой проект. Они являются стандартными для C++ и не требуют исключений или RTTI. 
Предполагая, что вы создаете отладочную версию своего проекта с помощью _DEBUG или DEBUG (а это делают все), MicroPather выполнит дополнительную проверку в этих режимах.
Пример использования: <a href="https://github.com/leethomason/MicroPather?ysclid=lh8l7305nc388997126#integrating-micropather-into-your-code">GitHub - leethomason/MicroPather: MicroPather is a path finder and A* solver (astar or a-star) written in platform independent C++ that can be easily integrated into existing code. MicroPather focuses on being a path finding engine for video games but is a generic A* solver.
<p>
<h2><strong>4.Таблица семантического аннотирования</strong></h2>
<br>
Micropather.h


<table class="MsoTableGrid" style="border-collapse:collapse;mso-table-layout-alt:fixed;border:none;
 mso-border-alt:solid black .5pt;mso-border-themecolor:text1;mso-yfti-tbllook:
 1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt" width="688" cellspacing="0" cellpadding="0" border="1">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">№</span></p>
  </td>
  <td style="width:86.4pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-left:none;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">Идиома</span></p>
  </td>
  <td style="width:325.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-left:none;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">Строки кода</span></p>
  </td>
  <td style="width:78.7pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-left:none;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">Комментарии</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">1</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/c#compile-time-const-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">compile
  time constant</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  layout-grid-mode:line"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">39</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,42,45,51,59,62,62,68</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">DEBUG</span><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line"> не путать с _</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">DEBUG</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line"></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">2</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Защита заголовка</span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">26</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,27,508</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">3</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#implicit-prologue-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">implicit
  prologue</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">44,47,61,64</span><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">,73,</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">76,77</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">4</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Управление ходом программы на этапе
  компиляции</span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">41-46</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">49-53</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">56-69</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,72-82,</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">86-130</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,246-255,493-495</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">5</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Директивы препроцессора</span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">59</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,60,61,62,</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">72(5-15)</span><span style="font-size:14.0pt;font-family:
  &quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,75(5-15)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">6</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Системные макросы</span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">62(</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">120-135</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">7</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/c#declare-namespace-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">declare
  namespace</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">84</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">8</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#typedef-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">typedef</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">74,78,81</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">9</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#if-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">if</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">12,22,29,30,115,258-261</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">10</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#while-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">while</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">13,20,21,27</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">11</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#for-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">for</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">32,367</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">12</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#switch-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">switch</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">19</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:13">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">13</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#break-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">break</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">24,34</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:14">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">14</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;line-height:
  normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#printf-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US" lang="EN-US">write formatted string to stdout</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US" lang="EN-US"><br style="mso-special-character:line-break">
  <br style="mso-special-character:line-break">
  </span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">23</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:15">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">15</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#call-func-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">call</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">26(5-14),99,102(45-54),105(50-60),118,119,213,214,249,251,252</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:16">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">16</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#str-to-num-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">string to number</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">32</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">Проверка ввода</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:17">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">17</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#num-to-str-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">number to string</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">30</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">Проверка ввода</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:18">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">1</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">8</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#define-generic"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA;background:#EEEEEE">define
  generic type</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">92</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,93</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:19">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">19</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#constructor"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA;background:#EEEEEE">constructor</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">95,274,375,399,451,486</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:20">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">20</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#destructor"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">destructor</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">96,162,275,376,452</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:21">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">21</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#destroy-object"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">destroy object</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">95(8-15),121</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:22">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">21</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#no-retval-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA;background:#EEEEEE">no
  return value</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">98,99</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:23">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">22</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#def-func-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">define</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">98,99-101</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:24">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">23</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;line-height:
  normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#retval-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">return</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA;
  mso-ansi-language:EN-US"> </span><span style="font-size:14.0pt;font-family:
  &quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">value</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black"><br style="mso-special-character:line-break">
  <br style="mso-special-character:line-break">
  </span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US" lang="EN-US"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">103,106,111(30-40),320(20-30),321(20-30),356,357,371,383(30-40),384(30-40)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:25">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">24</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;line-height:
  normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#incr-decr-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">increment and
  decrement</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">109,367(40-45)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:26">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">25</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#overload-op-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">overload operator</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">102,105,266,487</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:27">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">26</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#access-control"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">access control</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">94,113,264,273,312,350,389,417,485</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:28">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">27</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#unsigned-type-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">unsigned
  type</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">81(6-15),111,114(20-30),116,126,127,205(35-44),223,274(30-40,41-48),292,310,319,320,321,322(10-18),335,336,337,339,340,364,365,451(30-41,41-50),503</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:29">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">28</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#allocate-heap-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA;
  background:#EEEEEE">allocate heap</span></a><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">117(28-42)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:30">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">29</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#copy-fixed-len-array-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">copy</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">120</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:31">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">30</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#type-size-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">type size</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">120(30-50),367(30-45)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:32">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">31</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#struct-definition"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">struct
  definition</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">138-142,191-195,314-317,351-373,398-406</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:33">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">32</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#float-type-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">float type</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">141,207,208,219,220,221,223,294,295,361,381(40-50),402,406,463(60-70),474(40-51),500(10-15)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:34">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">33</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#define-class"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">define class</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">93,159-186,189,202-267,271-341,348-396,413-508</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:35;height:37.45pt">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:37.45pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">34</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:37.45pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#define-method"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">define method</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:37.45pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">98,99-101,108,111,114,170,178,185,205,211,212-216,235-239,240-245,247-254,257-262,278,292-296,299,302,306,310,323,324,363-373,378,379,380,383,384,463,474,479,482,483,489,491</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:37.45pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:36">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">35</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#dynamic-dispatch"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">dynamic dispatch</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">162,170,178,185</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:37">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">36</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Чистые виртуальные функции</span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">170,178,185</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:38">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">37</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#float-limits-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">float
  limits</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">214(15-20,24-29),258(30-36,40-46),261(0-26)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:39">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">38</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#create-object"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">create object</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">193,222,229,230,497,498,499,500,502,504</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:40">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">39</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#int-type-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">integer type</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">226,227,302(27-31,32-38),306(20-26,26-31),331,332,380(40-51),381,386,387,394,395,400,401,404,405,463</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:41">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">40</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#boolean-type-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">boolean
  type</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">222,223,356,357,451(50-61)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:42">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">41</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#receiver"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">name of receiver</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">215,241</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:43">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">42</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#multiple-line-comment-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">multiple
  line comment</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">1-23,30-38,146-157,409-412,420-450</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">Комментарии для понимания библеотеки и ее возможных адаптаций</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:44">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">43</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#write-once-var-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">write-once
  variable</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">302(20-26),356(19-30),364,379(20-30,30-40),390,391</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:45">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">44</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Константные функции</span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">320</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,321,356,357,363,383,384</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:46">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">45</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#bit-op-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">bit operators</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">320(20-24),321(21-25)</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:47">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">46</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#compound-assignment-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">compound
  assignment</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">368,369</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:48">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">47</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Дружественный класс</span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">415</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:49">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">48</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#enum-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">enum</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">418-426</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">Состояния решения</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:50;mso-yfti-lastrow:yes">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">49</span></p>
  </td>
  <td style="width:86.4pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="115" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#binary-octal-hex-literals-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  color:#0000AA;mso-ansi-language:EN-US" lang="EN-US">binary, octal, and hex literals</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US" lang="EN-US"></span></p>
  </td>
  <td style="width:325.8pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="434" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">365</span></p>
  </td>
  <td style="width:78.7pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="105" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">Создание</span><span style="font-size:14.0pt;font-family:
  &quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">
  Hash</span></p>
  </td>
 </tr>
</tbody></table>
Micropather.cpp
<!--[if gte mso 9]><xml>
 <o:OfficeDocumentSettings>
  <o:AllowPNG/>
 </o:OfficeDocumentSettings>
</xml><![endif]--><!--[if gte mso 9]><xml>
 <w:WordDocument>
  <w:View>Normal</w:View>
  <w:Zoom>0</w:Zoom>
  <w:TrackMoves/>
  <w:TrackFormatting/>
  <w:PunctuationKerning/>
  <w:ValidateAgainstSchemas/>
  <w:SaveIfXMLInvalid>false</w:SaveIfXMLInvalid>
  <w:IgnoreMixedContent>false</w:IgnoreMixedContent>
  <w:AlwaysShowPlaceholderText>false</w:AlwaysShowPlaceholderText>
  <w:DoNotPromoteQF/>
  <w:LidThemeOther>RU</w:LidThemeOther>
  <w:LidThemeAsian>X-NONE</w:LidThemeAsian>
  <w:LidThemeComplexScript>X-NONE</w:LidThemeComplexScript>
  <w:Compatibility>
   <w:BreakWrappedTables/>
   <w:SnapToGridInCell/>
   <w:WrapTextWithPunct/>
   <w:UseAsianBreakRules/>
   <w:DontGrowAutofit/>
   <w:SplitPgBreakAndParaMark/>
   <w:DontVertAlignCellWithSp/>
   <w:DontBreakConstrainedForcedTables/>
   <w:DontVertAlignInTxbx/>
   <w:Word11KerningPairs/>
   <w:CachedColBalance/>
  </w:Compatibility>
  <m:mathPr>
   <m:mathFont m:val="Cambria Math"/>
   <m:brkBin m:val="before"/>
   <m:brkBinSub m:val="&#45;-"/>
   <m:smallFrac m:val="off"/>
   <m:dispDef/>
   <m:lMargin m:val="0"/>
   <m:rMargin m:val="0"/>
   <m:defJc m:val="centerGroup"/>
   <m:wrapIndent m:val="1440"/>
   <m:intLim m:val="subSup"/>
   <m:naryLim m:val="undOvr"/>
  </m:mathPr></w:WordDocument>
</xml><![endif]--><!--[if gte mso 9]><xml>
 <w:LatentStyles DefLockedState="false" DefUnhideWhenUsed="true"
  DefSemiHidden="true" DefQFormat="false" DefPriority="99"
  LatentStyleCount="267">
  <w:LsdException Locked="false" Priority="0" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Normal"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="heading 1"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 2"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 3"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 4"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 5"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 6"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 7"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 8"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 9"/>
  <w:LsdException Locked="false" Priority="39" Name="toc 1"/>
  <w:LsdException Locked="false" Priority="39" Name="toc 2"/>
  <w:LsdException Locked="false" Priority="39" Name="toc 3"/>
  <w:LsdException Locked="false" Priority="39" Name="toc 4"/>
  <w:LsdException Locked="false" Priority="39" Name="toc 5"/>
  <w:LsdException Locked="false" Priority="39" Name="toc 6"/>
  <w:LsdException Locked="false" Priority="39" Name="toc 7"/>
  <w:LsdException Locked="false" Priority="39" Name="toc 8"/>
  <w:LsdException Locked="false" Priority="39" Name="toc 9"/>
  <w:LsdException Locked="false" Priority="35" QFormat="true" Name="caption"/>
  <w:LsdException Locked="false" Priority="10" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Title"/>
  <w:LsdException Locked="false" Priority="1" Name="Default Paragraph Font"/>
  <w:LsdException Locked="false" Priority="11" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Subtitle"/>
  <w:LsdException Locked="false" Priority="22" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Strong"/>
  <w:LsdException Locked="false" Priority="20" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Emphasis"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="false"
   UnhideWhenUsed="false" Name="Table Grid"/>
  <w:LsdException Locked="false" UnhideWhenUsed="false" Name="Placeholder Text"/>
  <w:LsdException Locked="false" Priority="1" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="No Spacing"/>
  <w:LsdException Locked="false" Priority="60" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Shading"/>
  <w:LsdException Locked="false" Priority="61" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light List"/>
  <w:LsdException Locked="false" Priority="62" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Grid"/>
  <w:LsdException Locked="false" Priority="63" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 1"/>
  <w:LsdException Locked="false" Priority="64" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 2"/>
  <w:LsdException Locked="false" Priority="65" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 1"/>
  <w:LsdException Locked="false" Priority="66" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 2"/>
  <w:LsdException Locked="false" Priority="67" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 1"/>
  <w:LsdException Locked="false" Priority="68" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 2"/>
  <w:LsdException Locked="false" Priority="69" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 3"/>
  <w:LsdException Locked="false" Priority="70" SemiHidden="false"
   UnhideWhenUsed="false" Name="Dark List"/>
  <w:LsdException Locked="false" Priority="71" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Shading"/>
  <w:LsdException Locked="false" Priority="72" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful List"/>
  <w:LsdException Locked="false" Priority="73" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Grid"/>
  <w:LsdException Locked="false" Priority="60" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Shading Accent 1"/>
  <w:LsdException Locked="false" Priority="61" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light List Accent 1"/>
  <w:LsdException Locked="false" Priority="62" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Grid Accent 1"/>
  <w:LsdException Locked="false" Priority="63" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 1 Accent 1"/>
  <w:LsdException Locked="false" Priority="64" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="65" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 1 Accent 1"/>
  <w:LsdException Locked="false" UnhideWhenUsed="false" Name="Revision"/>
  <w:LsdException Locked="false" Priority="34" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="List Paragraph"/>
  <w:LsdException Locked="false" Priority="29" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Quote"/>
  <w:LsdException Locked="false" Priority="30" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Intense Quote"/>
  <w:LsdException Locked="false" Priority="66" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="67" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 1 Accent 1"/>
  <w:LsdException Locked="false" Priority="68" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="69" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 3 Accent 1"/>
  <w:LsdException Locked="false" Priority="70" SemiHidden="false"
   UnhideWhenUsed="false" Name="Dark List Accent 1"/>
  <w:LsdException Locked="false" Priority="71" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Shading Accent 1"/>
  <w:LsdException Locked="false" Priority="72" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful List Accent 1"/>
  <w:LsdException Locked="false" Priority="73" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Grid Accent 1"/>
  <w:LsdException Locked="false" Priority="60" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Shading Accent 2"/>
  <w:LsdException Locked="false" Priority="61" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light List Accent 2"/>
  <w:LsdException Locked="false" Priority="62" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Grid Accent 2"/>
  <w:LsdException Locked="false" Priority="63" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 1 Accent 2"/>
  <w:LsdException Locked="false" Priority="64" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="65" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 1 Accent 2"/>
  <w:LsdException Locked="false" Priority="66" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="67" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 1 Accent 2"/>
  <w:LsdException Locked="false" Priority="68" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="69" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 3 Accent 2"/>
  <w:LsdException Locked="false" Priority="70" SemiHidden="false"
   UnhideWhenUsed="false" Name="Dark List Accent 2"/>
  <w:LsdException Locked="false" Priority="71" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Shading Accent 2"/>
  <w:LsdException Locked="false" Priority="72" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful List Accent 2"/>
  <w:LsdException Locked="false" Priority="73" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Grid Accent 2"/>
  <w:LsdException Locked="false" Priority="60" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Shading Accent 3"/>
  <w:LsdException Locked="false" Priority="61" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light List Accent 3"/>
  <w:LsdException Locked="false" Priority="62" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Grid Accent 3"/>
  <w:LsdException Locked="false" Priority="63" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 1 Accent 3"/>
  <w:LsdException Locked="false" Priority="64" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="65" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 1 Accent 3"/>
  <w:LsdException Locked="false" Priority="66" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="67" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 1 Accent 3"/>
  <w:LsdException Locked="false" Priority="68" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="69" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 3 Accent 3"/>
  <w:LsdException Locked="false" Priority="70" SemiHidden="false"
   UnhideWhenUsed="false" Name="Dark List Accent 3"/>
  <w:LsdException Locked="false" Priority="71" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Shading Accent 3"/>
  <w:LsdException Locked="false" Priority="72" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful List Accent 3"/>
  <w:LsdException Locked="false" Priority="73" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Grid Accent 3"/>
  <w:LsdException Locked="false" Priority="60" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Shading Accent 4"/>
  <w:LsdException Locked="false" Priority="61" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light List Accent 4"/>
  <w:LsdException Locked="false" Priority="62" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Grid Accent 4"/>
  <w:LsdException Locked="false" Priority="63" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 1 Accent 4"/>
  <w:LsdException Locked="false" Priority="64" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="65" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 1 Accent 4"/>
  <w:LsdException Locked="false" Priority="66" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="67" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 1 Accent 4"/>
  <w:LsdException Locked="false" Priority="68" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="69" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 3 Accent 4"/>
  <w:LsdException Locked="false" Priority="70" SemiHidden="false"
   UnhideWhenUsed="false" Name="Dark List Accent 4"/>
  <w:LsdException Locked="false" Priority="71" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Shading Accent 4"/>
  <w:LsdException Locked="false" Priority="72" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful List Accent 4"/>
  <w:LsdException Locked="false" Priority="73" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Grid Accent 4"/>
  <w:LsdException Locked="false" Priority="60" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Shading Accent 5"/>
  <w:LsdException Locked="false" Priority="61" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light List Accent 5"/>
  <w:LsdException Locked="false" Priority="62" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Grid Accent 5"/>
  <w:LsdException Locked="false" Priority="63" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 1 Accent 5"/>
  <w:LsdException Locked="false" Priority="64" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="65" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 1 Accent 5"/>
  <w:LsdException Locked="false" Priority="66" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="67" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 1 Accent 5"/>
  <w:LsdException Locked="false" Priority="68" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="69" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 3 Accent 5"/>
  <w:LsdException Locked="false" Priority="70" SemiHidden="false"
   UnhideWhenUsed="false" Name="Dark List Accent 5"/>
  <w:LsdException Locked="false" Priority="71" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Shading Accent 5"/>
  <w:LsdException Locked="false" Priority="72" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful List Accent 5"/>
  <w:LsdException Locked="false" Priority="73" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Grid Accent 5"/>
  <w:LsdException Locked="false" Priority="60" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Shading Accent 6"/>
  <w:LsdException Locked="false" Priority="61" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light List Accent 6"/>
  <w:LsdException Locked="false" Priority="62" SemiHidden="false"
   UnhideWhenUsed="false" Name="Light Grid Accent 6"/>
  <w:LsdException Locked="false" Priority="63" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 1 Accent 6"/>
  <w:LsdException Locked="false" Priority="64" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Shading 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="65" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 1 Accent 6"/>
  <w:LsdException Locked="false" Priority="66" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium List 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="67" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 1 Accent 6"/>
  <w:LsdException Locked="false" Priority="68" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="69" SemiHidden="false"
   UnhideWhenUsed="false" Name="Medium Grid 3 Accent 6"/>
  <w:LsdException Locked="false" Priority="70" SemiHidden="false"
   UnhideWhenUsed="false" Name="Dark List Accent 6"/>
  <w:LsdException Locked="false" Priority="71" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Shading Accent 6"/>
  <w:LsdException Locked="false" Priority="72" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful List Accent 6"/>
  <w:LsdException Locked="false" Priority="73" SemiHidden="false"
   UnhideWhenUsed="false" Name="Colorful Grid Accent 6"/>
  <w:LsdException Locked="false" Priority="19" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Subtle Emphasis"/>
  <w:LsdException Locked="false" Priority="21" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Intense Emphasis"/>
  <w:LsdException Locked="false" Priority="31" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Subtle Reference"/>
  <w:LsdException Locked="false" Priority="32" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Intense Reference"/>
  <w:LsdException Locked="false" Priority="33" SemiHidden="false"
   UnhideWhenUsed="false" QFormat="true" Name="Book Title"/>
  <w:LsdException Locked="false" Priority="37" Name="Bibliography"/>
  <w:LsdException Locked="false" Priority="39" QFormat="true" Name="TOC Heading"/>
 </w:LatentStyles>
</xml><![endif]--><!--[if gte mso 10]>
<style>
 /* Style Definitions */
 table.MsoNormalTable
	{mso-style-name:"Обычная таблица";
	mso-tstyle-rowband-size:0;
	mso-tstyle-colband-size:0;
	mso-style-noshow:yes;
	mso-style-priority:99;
	mso-style-qformat:yes;
	mso-style-parent:"";
	mso-padding-alt:0cm 5.4pt 0cm 5.4pt;
	mso-para-margin-top:0cm;
	mso-para-margin-right:0cm;
	mso-para-margin-bottom:8.0pt;
	mso-para-margin-left:0cm;
	line-height:107%;
	mso-pagination:widow-orphan;
	font-size:11.0pt;
	font-family:"Calibri","sans-serif";
	mso-ascii-font-family:Calibri;
	mso-ascii-theme-font:minor-latin;
	mso-fareast-font-family:"Times New Roman";
	mso-fareast-theme-font:minor-fareast;
	mso-hansi-font-family:Calibri;
	mso-hansi-theme-font:minor-latin;
	mso-bidi-font-family:"Times New Roman";
	mso-bidi-theme-font:minor-bidi;}
table.MsoTableGrid
	{mso-style-name:"Сетка таблицы";
	mso-tstyle-rowband-size:0;
	mso-tstyle-colband-size:0;
	mso-style-priority:39;
	mso-style-unhide:no;
	border:solid black 1.0pt;
	mso-border-themecolor:text1;
	mso-border-alt:solid black .5pt;
	mso-border-themecolor:text1;
	mso-padding-alt:0cm 5.4pt 0cm 5.4pt;
	mso-border-insideh:.5pt solid black;
	mso-border-insideh-themecolor:text1;
	mso-border-insidev:.5pt solid black;
	mso-border-insidev-themecolor:text1;
	mso-para-margin:0cm;
	mso-para-margin-bottom:.0001pt;
	mso-pagination:widow-orphan;
	font-size:11.0pt;
	font-family:"Calibri","sans-serif";
	mso-ascii-font-family:Calibri;
	mso-ascii-theme-font:minor-latin;
	mso-hansi-font-family:Calibri;
	mso-hansi-theme-font:minor-latin;
	mso-bidi-font-family:"Times New Roman";
	mso-bidi-theme-font:minor-bidi;
	mso-fareast-language:EN-US;}
</style>
<![endif]-->

<table class="MsoTableGrid" style="border-collapse:collapse;mso-table-layout-alt:fixed;border:none;
 mso-border-alt:solid black .5pt;mso-border-themecolor:text1;mso-yfti-tbllook:
 1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt" width="659" cellspacing="0" cellpadding="0" border="1">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:25.65pt">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:25.65pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">№</span></p>
  </td>
  <td style="width:125.1pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-left:none;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:25.65pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">Идиома</span></p>
  </td>
  <td style="width:224.05pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-left:none;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:25.65pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">Строки кода</span></p>
  </td>
  <td style="width:120.5pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-left:none;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:25.65pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">Комментарии</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">1</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#implicit-prologue-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">implicit
  prologue</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">31,32,40</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">2</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Управление ходом программы на этапе
  компиляции</span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">26-29</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,39-41,55-57,83-87,113-115,121-125,132-136,185-189,206-210,241-243,572-575,578-587,559-591,597-656,660-679,797-799,861-867,877-879,882-884,961-963,1065-1071</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">3</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Директивы препроцессора</span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">206(2-10),223(2-10)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">4</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Системные макросы</span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">653(38-39,41-46),757(19-24),767(20-25),1025(20-25)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">5</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/c#declare-namespace-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">declare
  namespace</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">45</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">6</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#if-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">if</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">95-99,142-145,148-160,395-411,527-549,551-570,732-734,837-849,871,874-885,937-958</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">7</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#while-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">while</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">93-101,152-153,397-406,435-442,519-523,543-548,793-801,902-960,1012-1052</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">8</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#for-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">for</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">314-316,556-565,629-633,650-655,691-698,736-746,1056-1064,1066-1069</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">9</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#break-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">break</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">98,438,441,800</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">10</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;line-height:
  normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#printf-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US" lang="EN-US">write formatted string to stdout</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US" lang="EN-US"><br style="mso-special-character:line-break">
  <br style="mso-special-character:line-break">
  </span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a name="_GoBack"></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">84,86,122,124,133,135,188,242,573,580,590,862,865,866</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">11</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#call-func-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">call</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">80,81,91,102,117,118,138,791,803,1025,1030,1068</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">12</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#constructor"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA;background:#EEEEEE">constructor</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">50-58,68,203-205,480-491,892-896</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:13">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">13</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#destructor"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">destructor</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">59,,494-497</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:14">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">14</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#no-retval-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA;background:#EEEEEE">no
  return value</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">261,269,393,510,595,789,833</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:15">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">15</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;line-height:
  normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#retval-note"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">return</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA;
  mso-ansi-language:EN-US"> </span><span style="font-size:14.0pt;font-family:
  &quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">value</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:black"><br style="mso-special-character:line-break">
  <br style="mso-special-character:line-break">
  </span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US" lang="EN-US"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">65,127,317,389,500,733,782,785,968,1073</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:16">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">16</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;line-height:
  normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#incr-decr-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">increment and
  decrement</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">386,388,761,781,784,807,887,1066,1067</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:17">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">17</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#overload-op-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">overload operator</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">69</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:18">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">18</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#access-control"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">access control</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">49,67,165,196</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:19">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">19</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#unsigned-type-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">unsigned
  type</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">321,416,556,560,625,818,1066,1067</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:20">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">20</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#allocate-heap-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA;
  background:#EEEEEE">allocate heap</span></a><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">227(10-90),704</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:21">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">21</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#type-size-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">type size</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">72,310(36-54,55-61)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:22">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">22</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#float-type-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">float type</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">840(30-35),845(28-32),1026</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:23">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">23</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#define-class"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">define class</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">47-74,,163-200,</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:24;height:37.45pt">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:37.45pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">24</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:37.45pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#define-method"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">define method</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:37.45pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">61,62,63,65,77-106,130-160,169-181,247-258,261-266,269-305,308-318,373-390,393-411,414-427,456-470,473-478,500-507,510-599,682-686,689-699,702-710,730-747,750-760,763-786,781-811,814-830,833-851,855-969,972-1053</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt;height:37.45pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:25">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">25</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#float-limits-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">float
  limits</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">91(20-27)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:26">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">26</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#create-object"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">create object</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">817,889,890</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:27">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">27</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#int-type-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">integer type</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">855</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:28">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">28</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#boolean-type-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">boolean
  type</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">65,247</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:29">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">29</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#receiver"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">name of receiver</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">166(30-35),475(5-10)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:30">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">30</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#multiple-line-comment-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">multiple
  line comment</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">220-221,323-369,661-678,974-995</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">Комментарии для понимания библеотеки и ее возможных адаптаций</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:31">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">31</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#write-once-var-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">write-once
  variable</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">68(10-15),69(12-17),197(15-21),198(16-22),625,626</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:32">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">32</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Константные </span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US" lang="EN-US">методы</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">814</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:33">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">33</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#compound-assignment-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;color:#0000AA">compound
  assignment</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">254(15-17),279(14-16),313(9-11),778(12-14)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:34">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">34</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Изменение поведения предупреждающих
  сообщений компилятора</span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">27</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,28</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">Отключения обработчика исключений<br>
  и<br>
  Усечение дебагером имен<br>
  (Необходимо для корректной работы </span><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:EN-US;
  layout-grid-mode:line" lang="EN-US">STL</span><span style="font-size:14.0pt;font-family:
  &quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line"> и </span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">MVC</span><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">)</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:35">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">35</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#invoke-method"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">invoke method</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US" lang="EN-US"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">54(30-40),56(35-45),96,112,114,123,134,143,144,150,173,229,237,447,448,449,450,513,558,644,646,684,685,758,820,823,859,943,953,956,1047,1050,1054</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:36">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">36</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#struct-member-access"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">struct member
  access</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">65(38-45),85(42-47),86(45-50),91(10-14),92(15-21),95(20-25,26-31),97(10-15),100(10-15),102(7-11),111(20-30),117(11-17),118(11-17),119(7-11),123(10-14),124(11-15),134(30-40),135(40-50),138(15-25),142(15-20,25-30,35-40,40-46),144(20-25),148(20-25,26-30,30-35),149(10-15),153(10-14),685,696,772,773,950,951,952,1057(40-45),1059(25-32),1060(27-34)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:37">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">37</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Динамическое форматирование</span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">86(14-21)</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">,135(29-41)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">Выводит двоичное число с точностью до 0.1</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:38">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">38</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#free-fixed-len-array-heap-note"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">free heap</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">238-240,715</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">&nbsp;</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:39">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">39</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US" lang="EN-US">memset</span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">297,705</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">(</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">http</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">://</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">cppstudio</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">.</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">com</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">/</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">post</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">/673/)<br>
  Функции </span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">Clear</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">() и </span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">Reset</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">() вызываются часто поэтому используется </span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">memset</span><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line"> для оптимизации</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:40">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">40</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><a href="https://hyperpolyglot.org/cpp#true-false-note"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">true and false</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US" lang="EN-US"></span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">93,255,397,793,819</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:41">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">41</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">Явное приведение типа</span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:line">732(25-29)</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">\,</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">840</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  mso-ansi-language:EN-US;layout-grid-mode:line" lang="EN-US">(40-45,52-57),845(40-45,52-57)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:42">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">42</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US" lang="EN-US">GLOUTPUT</span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">798,878,883</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;layout-grid-mode:
  line">?как то связано с </span><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:EN-US;layout-grid-mode:
  line" lang="EN-US">OpenGl</span><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;
  layout-grid-mode:line">?</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:43">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">43</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <h2 style="line-height:normal;mso-outline-level:2"><a href="https://hyperpolyglot.org/cpp#continue"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;font-weight:normal;mso-bidi-font-weight:
  bold">continue</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></h2>
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US" lang="EN-US">&nbsp;</span></p>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">926,1019,1035</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:44;mso-yfti-lastrow:yes">
  <td style="width:24.8pt;border:solid black 1.0pt;
  mso-border-themecolor:text1;border-top:none;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="33" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">44</span></p>
  </td>
  <td style="width:125.1pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="167" valign="top">
  <h2 style="line-height:normal;mso-outline-level:2"><a href="https://hyperpolyglot.org/cpp#coalesce"><span style="font-size:14.0pt;
  font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;font-weight:normal;mso-bidi-font-weight:
  bold">coalesce</span></a><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;"></span></h2>
  <h2 style="line-height:normal;mso-outline-level:2"><span style="font-size:
  14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;">&nbsp;</span></h2>
  </td>
  <td style="width:224.05pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="299" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;text-align:
  justify;line-height:normal;mso-pagination:none"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">398(40-41),423(35-36,878(54-55),931(39-40),932(41-42),1028(40-41),1029(42-43),1031(35-36)</span></p>
  </td>
  <td style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid black 1.0pt;mso-border-right-themecolor:text1;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;mso-border-left-alt:solid black .5pt;
  mso-border-left-themecolor:text1;mso-border-alt:solid black .5pt;mso-border-themecolor:
  text1;padding:0cm 5.4pt 0cm 5.4pt" width="161" valign="top">
  <p class="MsoNormal" style="margin-bottom:0cm;margin-bottom:.0001pt;
  text-align:center;line-height:normal;mso-pagination:none" align="center"><span style="font-size:14.0pt;font-family:&quot;Times New Roman&quot;,&quot;serif&quot;;mso-ansi-language:
  EN-US;layout-grid-mode:line" lang="EN-US">-</span></p>
  </td>
 </tr>
</tbody></table>



