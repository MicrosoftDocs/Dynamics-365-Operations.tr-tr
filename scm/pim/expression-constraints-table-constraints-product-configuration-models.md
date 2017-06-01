---
title: "Ürün yapılandırma modellerindeki ifade kısıtlamaları ve tablo kısıtlamaları"
description: "Bu konuda ifade kısıtlamalarının ve tablo kısıtlamalarının kullanımı açıklanmaktadır. Kısıtlamalar ürünleri satış siparişi, satış teklifi, satınalma siparişi veya üretim emri için yapılandırdığınızda, seçebileceğiniz öznitelik değerlerini denetler. Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını veya tablo kısıtlamalarını kullanabilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0bad513590ec0b0d495664d81f2e5f92e162bdd7
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Ürün yapılandırma modellerindeki ifade kısıtlamaları ve tablo kısıtlamaları

[!include[banner](../includes/banner.md)]


Bu konuda ifade kısıtlamalarının ve tablo kısıtlamalarının kullanımı açıklanmaktadır. Kısıtlamalar ürünleri satış siparişi, satış teklifi, satınalma siparişi veya üretim emri için yapılandırdığınızda, seçebileceğiniz öznitelik değerlerini denetler. Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını veya tablo kısıtlamalarını kullanabilirsiniz. 

Kısıtlamalar ürünleri satış siparişi, satış teklifi, satınalma siparişi veya üretim emri için yapılandırdığınızda, seçebileceğiniz öznitelik değerlerini denetlemek için kullanılır. Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını veya tablo kısıtlamalarını kullanabilirsiniz.

## <a name="what-are-expression-constraints"></a>İfade kısıtlamaları nelerdir?
İfade kısıtlamaları, aritmetik ve Boole işleçlerini ve işlevlerini kullanan bir ifade tarafından belirlenir. Bir ifade kısıtlaması, ürün yapılandırma modelinde belirli bir bileşen için yazılır. Başka bir bileşen tarafından yeniden kullanılamaz veya bir başka bileşenle paylaşılamaz. Ancak, bir bileşen için ifade kısıtlamaları, bileşenin alt bileşenlerinin özniteliklerini referans gösterebilir.

## <a name="what-are-table-constraints"></a>Tablo kısıtlamaları nelerdir?
Tablo kısıtlamaları, bir ürün yapılandırdığınızda öznitelikler için izin verilen değerlerin birleşimlerini listeler. Tablo kısıtlaması tanımları genel olarak kullanılabilir. Ürün yapılandırma modelinde bir bileşen için bir tablo kısıtlaması oluşturduğunuzda, tablo kısıtlaması tanımı seçersiniz. İzin verilen birleşimleri oluşturmak için belirli türdeki öznitelikleri bileşenlere eklersiniz. Her öznitelik türü belirli bir değere sahiptir.

### <a name="example-of-a-table-constraint"></a>Bir tablo kısıtlaması örneği.

Bu örnek, hoparlör yapılandırmasını belirli bir kabin rengi ve ön cephesiyle nasıl sınırlandırabileceğinizi gösterir. İlk tablo, yapılandırma için genelde kullanılabilir olan kabin rengini ve ön cepheyi gösterir. Değerler **Kabin rengi**ve **Izgara rengi** öznitelik türleri için tanımlanır.

| Öznitelik türü | Değerler                      |
|----------------|-----------------------------|
| Kabin rengi | Siyah, Meşe, Pelesenk, Beyaz, |
| Izgara rengi    | Siyah, Metal, Beyaz         |

Sonraki tablo, **Renk ve kaplama** tablo kısıtlamasıyla tanımlanan birleşimlerini gösterir. Bu tablo kısıtlamasını kullanarak bir hoparlörü meşe kaplamalı ve siyah ızgaralı, pelesenk kaplamalı ve beyaz ızgaralı ve benzeri şekilde yapılandırabilirsiniz.

| Son         | Izgara                       |
|----------------|-----------------------------|
| Meşe            | Siyah                       |
| Venge       | Beyaz                       |
| Beyaz          | Siyah                       |
| Beyaz          | Beyaz                       |
| Siyah          | Siyah                       |
| Siyah          | Metal                       | 

Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları oluşturabilirsiniz. Daha fazla bilgi için, [Sistem tanımlı ve kullanıcı tanımlı tablo kısıtlamaları](system-defined-user-defined-table-constraints.md) bölümüne bakın.

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Kısıtlamaları yazmak için hangi sözdizimi kullanılmalıdır?
Kısıtlamaları yazarken En İyi Duruma Getirme Modelleme Dili (OML) sözdizimini kullanmalısınız. Sistem, kısıtlamaları çözümlemek için Microsoft Solver Foundation kısıtlama çözücüsünü kullanır.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Tablo kısıtlamaları veya ifade kısıtlamaları kullanmam gerekir mi?
Kısıtlamaları nasıl oluşturmayı tercih ettiğinizde bağlı olarak ifade kısıtlamalarını ya da tablo kısıtlamalarını kullanabilirsiniz. İfade kısıtlaması tek bir ifade olduğunda bir matris olarak tablo kısıtlaması oluşturursunuz. Bir ürünü yapılandırdığınızda, ne tür bir kısıtlama kullanıldığının önemi yoktur. Aşağıdaki örnekte iki yöntem arasındaki fark gösterilir.  

Bir ürünü aşağıdaki kısıtlama ayarlarını kullanarak yapılandırdığınızda bu kombinasyonlara izin verilir:

-   Siyah renkte ve boyutu 30 veya 50 olan bir ürün
-   Kırmızı renkte ve boyutu 20 olan bir ürün

### <a name="table-constraint-setup"></a>Tablo kısıtlaması ayarı

| Renk | Ebat |
|-------|------|
| Siyah | 30   |
| Siyah | 50   |
| Kırmızı   | 20   |

### <a name="expression-constraint-setup"></a>İfade kısıtlaması ayarı

(Renk == "Siyah" & (boyut == "30" | boyut == "50")) | (renk == "Kırmızı" & boyut = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>İfade kısıtlamaları yazarken bir işleç ya da parantezli yazım kullanmam gerekir mi?
Önek operatörleri ya da parantezli yazım kullanarak bir ifade kısıtlaması yazabilirsiniz. **Min**, **Mak** ve **Mutlak** işleçleri için parantezli yazım kullanamazsınız. Bu işleçler, çoğu programlama dilinde standart işleçler olarak dahil edilir.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>İfade kısıtlamaları yazarken hangi işleçleri ve parantezli yazımı kullanabilirim?
Aşağıdaki tablolarda, ürün yapılandırma modelinde bir bileşen için bir ifade kısıtlaması yazarken kullanabileceğiniz işleçler ve parantezli yazım listelenmiştir. İlk tablodaki örnekler parantezli yazım ya da işleçler kullanılarak bir ifadenin nasıl yazılacağını gösterir.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>İşleç</th>
<th>Açıklama</th>
<th>Sözdizimi</th>
<th>Örnekler</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implies</td>
<td>İlk koşul yanlış, ikinci koşul doğru ya da her ikisi de doğru ise bu doğrudur.</td>
<td>Implies[a, b], infix: a -: b</td>
<td><ul>
<li><strong>İşleç:</strong> Implies[x != 0, y &gt;= 0]</li>
<li><strong>Parantezli yazım:</strong> x != 0 -: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>Ve</td>
<td>Koşulların tümü doğru ise bu doğrudur. Koşulların sayısı 0 (sıfır) ise, <strong>Doğru</strong> değeri çıkar.</td>
<td>And[args], infix: a &amp; b &amp; ... &amp; z</td>
<td><ul>
<li><strong>İşleç:</strong> And[x == 2, y &lt;= 2]</li>
<li><strong>Parantezli yazım:</strong> x == 2 &amp; y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Veya</td>
<td>Herhangi bir koşul doğru ise bu doğrudur. Koşulların sayısı 0 (sıfır) ise, <strong>Yanlış</strong> değeri çıkar.</td>
<td>Or[args], infix: a | b | ... | z</td>
<td><ul>
<li><strong>İşleç:</strong> Or[x == 2, y &lt;= 2]</li>
<li><strong>Parantezli yazım:</strong> x == 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Artı</td>
<td>Bu, koşullarını toplar. Koşulların sayısı 0 (sıfır) ise, <strong>0</strong> değeri çıkar.</td>
<td>Plus[args], infix: a + b + ... + z</td>
<td><ul>
<li><strong>İşleç:</strong> Plus[x, y, 2] == z</li>
<li><strong>Parantezli yazım:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eksi</td>
<td>Bu, çıkarımı negatif hale getirir. Tek bir koşula sahip olması gerekir.</td>
<td>Minus[expr], infix: -expr</td>
<td><ul>
<li><strong>İşleç:</strong> Minus[x] == y</li>
<li><strong>Parantezli yazım:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>Bu, koşulunun mutlak değerini alır. Tek bir koşula sahip olması gerekir.</td>
<td>Abs[expr]</td>
<td><strong>İşleç:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Zaman</td>
<td>Bu, koşullarının ürününü alır. Koşulların sayısı 0 (sıfır) ise, <strong>1</strong> değeri çıkar.</td>
<td>Times[args], infix: a * b * ... * z</td>
<td><ul>
<li><strong>İşleç:</strong> Times[x, y, 2] == z</li>
<li><strong>Parantezli yazım:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Güç</td>
<td>Vu, üslü değer alır. Kuvveti sağdan sola uygular. (Diğer bir deyişle, sağa ilişkilendirilebilir.) Bu nedenle, <strong>Power[a, b, c]</strong> <strong>Power[, Power[b, c]]</strong> ile eşdeğerdir. <strong>Power</strong>, üs yalnızca pozitif bir sabit sayı ise kullanılabilir.</td>
<td>Power[args], infix: a ^ b ^ ... ^ z</td>
<td><ul>
<li><strong>İşleç:</strong> Power[x, 2] == y</li>
<li><strong>Parantezli yazım:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maks</td>
<td>Bu, en büyük koşulu oluşturur. Koşulların sayısı 0 (sıfır) ise, <strong>Sonsuzluk</strong> üretir.</td>
<td>Max[args]</td>
<td><strong>İşleç:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Minimum</td>
<td>Bu, en küçük koşulu oluşturur. Koşulların sayısı 0 (sıfır) ise, <strong>Sonsuzluk</strong> üretir.</td>
<td>Min[args]</td>
<td><strong>İşleç:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Not</td>
<td>Bu, koşulunun mantıksal tersini oluşturur. Tek bir koşula sahip olması gerekir.</td>
<td>Not[expr], infix: !expr</td>
<td><ul>
<li><strong>İşleç:</strong> Not[x] &amp; Not[y == 3]</li>
<li><strong>Parantezli yazım:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

Sonraki tablodaki örnekler parantezli yazımın nasıl yazılacağını gösterir.

| Parantezli yazım    | Açıklama                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| x + y + z         | Fark hesap eki                                                                                      |
| x \* y \* z       | Çarpma                                                                                |
| x - y             | İkili çıkarma, negatife düşmüş bir ikinci varsa ikili toplama ile aynı şekilde çevrilir. |
| x ^ y ^ z         | Sağa birleşimli üs                                                   |
| !x                | Boole değil                                                                                   |
| x -: y            | Boole çıkarım                                                                           |
|  x  | y | z         | Boole ya da                                                                                    |
| x & y & z         | Boole ve                                                                                   |
| x == y == z       | Denklik                                                                                      |
| x != y != z       | Benzersiz                                                                                      |
| x &lt; y &lt; z   | Küçüktür                                                                                     |
| x &gt; y &gt; z   | Büyüktür                                                                                  |
| x &lt;= y &lt;= z | Küçüktür veya eşittir                                                                         |
| x &gt;= y &gt;= z | Büyüktür veya eşittir                                                                      |
| (x)               | Parantezler varsayılan önceliği geçersiz kılar.                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>İfade kısıtlamalarım neden hatasız doğrulanmıyor?
Ayrılmış anahtar sözcükleri, öznitelikleri, bileşenleri veya ürün yapılandırma modelinde alt bileşenleri için çözücü ad olarak kullanamazsınız. Kullanamayacağınız anahtar sözcüklerin bir listesi aşağıdadır:

-   Üst
-   Öğe
-   Eşit
-   Kat
-   Eğer
-   Küçüktür
-   Büyüktür
-   Gösterir
-   Hata İletileri
-   Maks
-   Minimum
-   Eksi
-   Artı
-   Güç
-   Zamanlar
-   Aralık
-   Model
-   Karar
-   Hedef


<a name="see-also"></a>Ayrıca bkz.
--------

[Bir ifade kısıtlaması oluşturma (Görev kılavuzu)](http://ax.help.dynamics.com/en/wiki/create-an-expression-constraint/)

[Bir ürün yapılandırma modeline hesaplama ekleme (Görev kılavuzu)](http://ax.help.dynamics.com/en/wiki/add-a-calculation-to-a-product-configuration-model/)




