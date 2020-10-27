---
title: Ürün yapılandırma modellerine genel bakış
description: Bu makalede, ürün yapılandırma modelleriyle ilgili koşullar ve kavramlar tanımlanmaktadır. Ürün yapılandırma modelleri, tek bir ürün için pek çok ürün çeşitleri yapılandırmak için kullanılan bir genel ürün yapısı oluşturmanızı sağlar.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage, PCModalWaitDialog, PCTemplateConfigurationManager, PCConfigurationUIGrouping
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87d61203d36722194b98a247609fa126b71b846c
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981170"
---
# <a name="product-configuration-models-overview"></a>Ürün yapılandırma modellerine genel bakış

[!include [banner](../includes/banner.md)]

Bu makalede, ürün yapılandırma modelleriyle ilgili koşullar ve kavramlar tanımlanmaktadır. Ürün yapılandırma modelleri, tek bir ürün için pek çok ürün çeşitleri yapılandırmak için kullanılan bir genel ürün yapısı oluşturmanızı sağlar.

Ürün yapılandırma modelleri genel bir ürün yapısını temsil etmek üzere oluşturulur. Bir ürün yapılandırma modeli ayarladıktan sonra benzersiz bir ürün reçetesi (BOM) ve benzersiz bir rotası olan farklı bir ürün çeşidi yapılandırabilirsiniz. Ürün yapılandırma modelleri hem bildirime dayalı kısıtlamalar hem de kesinlik temelli hesaplamaları kullanarak farklı ürün çeşitleri arasındaki ilişkileri ve sınırlamaları işler. Satış siparişleri, satış teklifleri, satınalma siparişleri ve üretim emirlerindeki öğeleri yapılandırabilirsiniz. Aşağıdaki tablo, tablo kısıtlaması tabanlı terimleri ve kavramları açıklar.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Bileşenler</td>
<td>Bileşenler, bir ürün yapılandırma modelinin ana yapı taşlarıdır. Bileşenleri <strong>Kısıtlama tabanlı ürün yapılandırma modeli ayrıntıları</strong> sayfasındaki bir ağaç yapısında görüntülenir. Bileşenler aşağıdaki öğeleri içerebilir:
<ul>
<li>Öznitelikler</li>
<li>Sınırlamalar</li>
<li>Hesaplamalar</li>
<li>Alt bileşenler</li>
<li>Kullanıcı gereksinimleri</li>
<li>Ürün reçetesi satırları</li>
<li>Rota işlemleri</li>
</ul></td>
</tr>
<tr class="even">
<td>Öznitelikler</td>
<td>Öznitelikler, ürün yapılandırma modelinin tüm özelliklerini açıklanmaktadır. Öznitelikleri farklı bir ürün yapılandırıldığında seçilebilir özellikleri belirtmek için kullanabilirsiniz. Öznitelikler kısıtlamalar ve şartlarda kullanılır. Öznitelikler oluşturulur ve ürün yapılandırma modeline eklenir, ilgili öznitelik türleri referans alınır. Bir öznitelik için bir varsayılan değer ayarlayabilirsiniz. Ürün yapılandırma modeli yapılandırıldığında, varsayılan değer yapılandırma kullanıcı arabiriminde (UI) kullanılır. Bir özniteliğin zorunlu, salt okunur veya gizli olduğunu belirtebilirsiniz.
<ul>
<li><strong>Zorunlu</strong> – ürün yapılandırıldığında, öznitelik için bir değer ayarlamanız gerekir.</li>
<li><strong>Salt okunur</strong> – öznitelik değeri yapılandırma oturumu sırasında görüntülenir, ancak değiştirilemez.</li>
<li><strong>Gizli</strong> – öznitelik değeri, kısıtlamalara ve koşullara dahil edilir ancak yapılandırma oturumu sırasında görüntülenmez.</li>
</ul>
Ayrıca, öznitelikler için bir koşul belirtebilirsiniz. Koşul karşılanırsa, zorunlu öznitelik için bir değer girilmelidir. Koşulların ürün yapılandırma modeline dahil edilebilmeleri için özniteliklerde, ürün reçetelerinde ve rota operasyonlarında karşılanmalıdır Bir koşulda referans gösterilen herhangi bir öznitelik zorunlu hale gelir. Öznitelikleri, <strong>Öznitelikler</strong> sekmesinde zorunlu olarak seçmenizi öneririz. Bu, zorunlu öznitelikleri belirlemeyi kolaylaştırabilir. Öznitelik değerleri yeniden yapılandırmaların önemli bir parçasıdır. Sistem yapılandırma oturumu sırasında kullanıcı tarafından yapılan seçimler ile eşleşen bir yapılandırma var olup olmadığını belirlemek için öznitelik değerlerini kullanır.</td>
</tr>
<tr class="odd">
<td>Öznitelik türleri</td>
<td>Öznitelik türleri, yapılandırma ürün modelinde öznitelikler için kullanılan veri türleri kümesini belirtir. Aşağıdaki öznitelik türleri kullanılır:
<ul>
<li>Bir aralıkta olan veya olmayan, <strong>Tamsayı</strong> .</li>
<li><strong>Ondalık</strong></li>
<li>Sabit bir listesi olan veya olmayan, <strong>Metin</strong> .</li>
<li><strong>Boole</strong></li>
</ul>
Eğer öznitelik türü <strong>Boolean</strong>, aralığa sahip bir <strong>Tamsayı</strong> veya sabit bir listesi olan <strong>Metin</strong> ise, bir ürün yapılandırma modeli ayarlanırken değerleri kümesi kullanılabilir. <strong>Not:</strong> Ürün yapılandırma çözüm sağlayıcısı yalnızca şu öznitelik türlerini tanır: <strong>Boolean</strong>, sabit listeye sahip <strong>Metin</strong> ve bir aralığa sahip <strong>Tamsayı</strong>. Bu nedenle, yalnızca bu öznitelik türleri deyim kısıtlamaları ve şartları için kullanılabilir.</td>
</tr>
<tr class="even">
<td>Sınırlamalar</td>
<td>Kısıtlamalar, ürün modeli yapılandırmasının kısıtlamalarını açıklamaktadır. Kısıtlamalar, bir ürün yapılandırılırken yalnızca geçerli değerlerin seçildiğini güvence altına almak için kullanılır. Kısıtlamalar ya ifade kısıtlamaları ya da tablo kısıtlamaları olabilirler.
<ul>
<li>İfade kısıtlamaları yalnızca bağlı oldukları bileşen için kullanılabilirler. Bir bileşen için deyim kısıtlamaları, bileşenin alt bileşenlerinin özniteliklerini referans gösterebilir. Ürün yapılandırma çözücüsü kısıtlamaları çözmek için kullanılır ve kısıtlamaları yazarken çözücü sözdizimi kullanmanız gerekir. Daha fazla bilgi için ifade kısıtlamaları ve tablo kısıtlamaları konu bağlantısına bakınız.</li>
<li>Ürün yapılandırma modelindeki bir bileşene uygulanabilmesi için tablo kısıtlamaları belirlenmelidir. Tablo kısıtlamaları kullanıcı tanımlı veya sistem tanımlı olabilir. Bir kullanıcı tanımlı tablo kısıtlaması öznitelik türleri tarafından tanımlanan öznitelik değerleri için bir dizi kombinasyonu tanımlamak için kullanılabilecek bir matris türüdür. Örneğin üretilecek şey bir hoparlör ise, kullanıcı tanımlı tablo kısıtlaması için matris, hoparlörün yüzey rengi için sütunlara sahip olabilir.</li>
</ul>
<strong>Örnek</strong> Hoperlörler dört yüzey rengine veya türüne sahip olabilir: Siyah, Meşe, Venge ve Beyaz. Hoparlörde üç ön ızgaradan biri bulunabilir: Siyah, Metal veya Beyaz. Siyah yüzey tüm ızgaralar için kullanılabilir, ancak diğerleri belirli ızgaralar için sınırlıdır. Aşağıdaki tablo <strong>Tablo kısıtlamasını düzenle</strong> sayfasındaki <strong>İzin verilen birleşimler</strong> sekmesindeki görüntülenen örnek bilgiyi gösterir.
<table>
<thead>
<tr class="header">
<th>Kabin rengi</th>
<th>Izgara rengi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Siyah</td>
<td>Siyah</td>
</tr>
<tr class="even">
<td>Siyah</td>
<td>Metal</td>
</tr>
<tr class="odd">
<td>Siyah</td>
<td>Beyaz</td>
</tr>
<tr class="even">
<td>Meşe</td>
<td>Siyah</td>
</tr>
<tr class="odd">
<td>Venge</td>
<td>Beyaz</td>
</tr>
<tr class="even">
<td>Beyaz</td>
<td>Siyah</td>
</tr>
<tr class="odd">
<td>Beyaz</td>
<td>Beyaz</td>
</tr>
</tbody>
</table>
Sistem tanımlı bir tablo kısıtlaması, bir Supply Chain Management tablosundaki bir alan ile bir öznitelik türü arasındaki eşlemeyi temsil eder. Sistem tanımlı tablo kısıtlaması öznitelik türünü alana dinamik olarak bağlar. Bağlantı, bir ürün yapılandırması modelindeki özniteliği Supply Chain Management tablosundaki alanlarda bulunan verileri göstermek üzere etkinleştirir.</td>
</tr>
<tr class="odd">
<td>Hesaplamalar</td>
<td>Hesaplamalar kısıtlamalar için bir ektir. <strong>Ondalık</strong> ve <strong>Tamsayı</strong> türlerindeki öznitelikler üzerinde aritmetik işlemler gerçekleştirmek için bir işlem yapmak veya sabit listeli <strong>Metin</strong> ve <strong>Boolean</strong> türleri için mantık işlemleri yapmak için hesaplamayı kullanabilirsiniz. Bir hesaplamanın, hesaplama ifadesinin sonucunu tutacak bir hedef özniteliği vardır. Hesaplama ifadesi, ifade düzenleyicisi kullanılarak üretilmiştir.</td>
</tr>
<tr class="even">
<td>Alt bileşenler</td>
<td>Alt bileşenler ürün yapılandırma modelinin ağaç yapısını yansıtır. Ürün yapılandırma modelinin yapısını oluşturmak için alt bileşenleri kullanabilirsiniz. Alt bileşenler mevcut bileşenleri referans gösterir. Bu nedenle alt bileşenler çok sayıda ürün yapılandırma modelindeki bileşenlerin yeniden kullanılmasını teşvik eder. Bir alt bileşen için <strong>Ürün reçetesi satırı ayrıntıları</strong> sayfası üzerinde, o alt bileşen için farklı bir değer seçebilirsiniz. Alternatif olarak, ürün yapılandırma modeli ayarlanırken değerin seçileceği bir özniteliği seçebilirsiniz. Bir ürünü bir bileşen veya alt bileşen olarak dahil etmek istiyorsanız,<strong> Ürün oluştur</strong> sayfasında aşağıdaki bilgileri ürünü oluşturduğunuzda belirlemeniz gerekir:
<ul>
<li><strong>Ürün türü</strong> alanında, <strong>Madde</strong>'yi seçin.</li>
<li><strong>Ürün alt türü</strong> alanında, <strong>Ana ürün</strong>'ü seçin.</li>
<li><strong>Yapılandırma teknolojisi</strong> alanında <strong>Kısıtlama tabanlı yapılandırma</strong>'yı seçin.</li>
</ul>
Yayınlanmış bir ürünün bileşen veya alt bileşen olarak kullanılıp kullanılamayacağınızı <strong>Serbest bırakılmış ürün ayrıntıları</strong> sayfasındaki <strong>Genel</strong> sekmesinde görebilirsiniz. <strong>Yapılandırma teknolojisi</strong> alanında <strong>Kısıtlama tabanlı yapılandırma</strong> seçiliyse, ürün bir bileşen veya alt bileşen olarak kullanılabilir. Bir yapılandırma oturumu sırasında bileşenleri kullanıcıya görünmemeleri için gizleyebilirsiniz. Alt bileşen ile ilintili öznitelikler, alt bileşenler ve kullanıcı gereksinimleri de gizlenir.</td>
</tr>
<tr class="odd">
<td>Kullanıcı gereksinimleri</td>
<td>Kullanıcı gereksinimleri, bir kullanıcının gereksinimlerini ve belirli bileşenler ve öznitelikler arasındaki bir soyutlamayı temsil eder. Bir öğeye bir kullanıcı gereksinimini eşleyemezsiniz. Örneğin, bir müşteri bir ev sineması sistemi almak istiyor. Satış Temsilcisi ihtiyaç duyulacak watt miktarını belirlemek için müşteriye sistemin kurulacağı odanın boyutunu sorabilir. Bu örnekte, oda büyüklüğü belirli bir bileşen için uygun öznitelik değerini saptamaya yardımcı olan bir kullanıcı gereksinimi olabilir. Bir yapılandırma oturumu sırasında gereksinimleri kullanıcıya görünmemeleri için gizleyebilirsiniz. Kullanıcı gereksinimleri ile ilintili öznitelikler, alt bileşenler ve kullanıcı gereksinimleri de gizlenir. Bir kullanıcı gereksiniminin gizli olup olmadığını denetlemek için bir koşul yazabilirsiniz. Durumu, En iyi duruma getirme Modelleme Dili (OML) sözdizimini kullanarak yazmalısınız.</td>
</tr>
<tr class="even">
<td>Ürün reçetesi satırları</td>
<td>Ürün reçetesi satırları, ürün yapılandırma modelindeki bileşenler için her bir malzemeyi temsil eder. <strong>Ürün reçetesi satırı ayrıntıları</strong> sayfasında, tüm maddeler seçilebilir. Ürün yapılandırma modeli ayarlandığında kullanıcının seçimleri taban alınarak, seçilen farklı ürün varyantı için ürün reçetesi satırlarının farklılık gösterebilmesi için, ürün reçetesi satırına bir koşul eklenebilir. Koşulların ürün yapılandırma modeline dahil edilebilmeleri için özniteliklerde, ürün reçetelerinde ve rota operasyonlarında karşılanmalıdır <strong>Ürün reçetesi satırı ayrıntıları</strong> sayfasında, farklı bir değer seçebilirsiniz. Alternatif olarak, ürün yapılandırma modeli ayarlanırken değerin seçileceği bir özniteliğe eşleyebilirsiniz.</td>
</tr>
<tr class="odd">
<td>Rota işlemleri</td>
<td><strong>Rota operasyonu ayrıntıları</strong> sayfasında, farklı bir değer seçebilirsiniz. Alternatif olarak, ürün yapılandırma modeli ayarlanırken değerin seçileceği bir özniteliğe eşleyebilirsiniz. Koşullar, ifade kısıtlamaları gibi yazılırlar. Koşulların ürün yapılandırma modeline dahil edilebilmeleri için özniteliklerde, ürün reçetelerinde ve rota operasyonlarında karşılanmalıdır</td>
</tr>
</tbody>
</table>





