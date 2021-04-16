---
title: Satıcı faturaları için muhasebe dağılımları ve defter girişleri
description: Muhasebe dağılımları, bir tutarın, örneğin giderin, verginin veya masrafların, bir satıcı faturasında nasıl hesaba katılacağını tanımlamak için kullanılır. Satıcı faturası günlüğe kaydedildiğinde hesaba katılması gereken tüm tutarlar, bir veya daha fazla muhasebe dağıtımına sahip olacaktır.
author: abruer
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 953069dfd39843d39cc92d99318f02819dc31ed0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820996"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Satıcı faturaları için muhasebe dağılımları ve defter girişleri

[!include [banner](../includes/banner.md)]

Muhasebe dağılımları, bir tutarın, örneğin giderin, verginin veya masrafların, bir satıcı faturasında nasıl hesaba katılacağını tanımlamak için kullanılır. Satıcı faturası günlüğe kaydedildiğinde hesaba katılması gereken tüm tutarlar, bir veya daha fazla muhasebe dağıtımına sahip olacaktır. 

<a name="accounting-distributions"></a>Muhasebe dağılımları 
-------------------------

Satıcı faturası sayfasında aşağıdaki düğmeleri kullanarak satıcı faturası üzerindeki her bir satır için muhasebe dağılımlarını görüntüleyebilir ve değiştirebilirsiniz
-   **Tutarları dağıtmak** – Vergiler ve masraflar gibi tek bir satır ve tüm alt satırların muhasebe dağılımlarını görüntüleyip değiştirin. Alt satır için muhasebe dağılımlarını da doğrudan satış vergisi hareketleri sayfasından veya Gider hareketlerini görüntüleyebilir ve değiştirebilirsiniz.
    -   Satıcı faturası başlığındaki gider veya para birimi yuvarlama gibi tutarları değiştirin.
    -   Satıcı faturası satırı tutarlarını değiştirin.
-   **Dağılımları görüntülemek** – Belge üzerindeki tüm satırların muhasebe dağılımlarını görüntüleyin. Muhasebe dağılımlarını bu görünümden değiştiremezsiniz.
    -   Başlığı ve satır tutarlarını görüntüleyin.

Satıcı faturası bir satınalma emrini referans alıyorsa, stoklanmamış bir madde içeren satırlar için muhasebe dağılımlarını bölüp değiştirebilirsiniz. Satıcı faturası satırı bir satınalma emri satırını referans almıyorsa, muhasebe dağılımını silmeniz de mümkündür. Masraflar, vergiler ve satır iskontoları için satırları bölemez veya silemezsiniz. Genel muhasebe hesabını değiştirebilirsiniz, ancak tutarları veya yüzdeleri değiştiremezsiniz.
> [!NOTE]                                                                                                                                 
> Ana satırda stoklanmamış bir madde varsa ve muhasebe dağılımları bölünmüşse, alt satır ana satırın mali boyutları ile eşleşecek şekilde otomatik olarak bölünecektir. Alt satır için muhasebe dağılımları ayrıca bölünemez veya silinemez ancak alt satırın kurulumuna bağlı olarak, alt satırın muhasebe dağılımlarına yönelik ana muhasebe hesabını değiştirebilirsiniz.

## <a name="distributing-amounts"></a>Dağılım tutarları
Satıcı faturası girdiğinizde, her tutar aşağıdaki şekilde dağılır.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Satıcı faturası satırının türü</th>
<th>Ana hesabın nereden görüntüleneceğini belirleyen öncelik sırası</th>
<th>Hangi varsayılan mali boyutun görüntüleneceğini belirleyen öncelik sırası</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Stoğu tutulan ürün</td>
<td><ol>
<li>Satınalma emri satırı için muhasebe dağılımı.</li>
<li>Deftere nakletme sayfasında Ürün için satınalma harcaması seçiliyken Ana muhasebe alanı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Satıcı faturası üzerindeki varsayılan mali boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="even">
<td>Bir tedarik kategori veya ürün stoklanmamış</td>
<td><ol>
<li>Satınalma emri satırı için muhasebe dağılımı, satıcı faturası satırı bir satınalma emri satırını referans alıyorsa.</li>
<li>Deftere nakletme sayfasında Harcama için satınalma harcaması seçiliyken Ana muhasebe alanı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</li>
<li>Satıcı faturası üzerindeki varsayılan mali boyut değerlerini kullanın.</li>
<li>Satıcı faturası satırından mali boyut değerlerini kullanın.</li>
<li>Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Sabit kıymet</td>
<td><ol>
<li>Satınalma emri satırı için muhasebe dağılımı, satıcı faturası satırı bir satınalma emri satırını referans alıyorsa.</li>
<li>Satıcı faturası formundaki Hareket türü alanında Alım seçili ise, Sabit kıymet nakil profilleri sayfasında Alım seçiliyken ise Ana muhasebe alanı.</li>
<li>Satıcı faturası formundaki Hareket türü alanında Alım ayarlama seçili ise, Sabit kıymet nakil profilleri sayfasında Alım seçiliyken ise Ana muhasebe alanı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Satıcı faturası satırından mali boyut değerlerini kullanın.</li>
<li>Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="even">
<td>Satıcı faturası satırında tanımlı proje</td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</li>
<li>Proje grupları sayfasındaki Maliyetleri naklet - madde alanında Bakiye seçili ise, Genel muhasebe defterine nakil ayarı sayfasında Maliyet seçiliyken Ana muhasebe alanı.</li>
<li>Proje grupları sayfasındaki Maliyetleri naklet - madde alanında Kar ve zarar seçili ise, Genel muhasebe defterine nakil ayarı sayfasında Maliyet - madde seçiliyken Ana muhasebe alanı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Satır iskontosu</td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</li>
<li>Nakil sayfasında İskonto seçiliyken Ana hesap alanı.</li>
<li>Bir iskonto için deftere nakil profilinde ana muhasebe tanımlı değilse, satınalma emri satırındaki genişletilmiş fiyatın muhasebe dağılımı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</li>
<li>Satıcı faturası satırı için mali boyut değerlerini kullanın.</li>
<li>Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="even">
<td>Satınalma emri satırının Fiyat ve iskonto sekmesine girilen satınalma masrafı</td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</li>
<li>Satınalma emri satırındaki genişletilmiş fiyatın muhasebe dağılımı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Satır masrafı</td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</li>
<li>Masraflar kodu formundaki borç Türü alanında Genel muhasebe seçili ise, Masraflar kodu sayfasındaki borç Hesabı alanı.</li>
<li>Masraflar kodu formundaki borç Türü alanında Madde seçiliyse, satınalma emri satırındaki genişletilmiş fiyat için muhasebe dağılımı.</li>
<li>Masraflar kodu formundaki borç Türü alanında Müşteri/Satıcı seçili ise, Masraflar kodu sayfasındaki kredi Hesabı alanı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</li>
<li>Satıcı faturası satırından mali boyut değerlerini kullanın.</li>
<li>Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="even">
<td>Aşağıdaki koşulla vergi:
<ul>
<li>Genel muhasebe parametreleri sayfasında ABD vergilendirme kurallarını uygula seçeneği seçili.</li>
</ul></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</li>
<li>Genişletilmiş fiyatın veya masrafın muhasebe dağılımı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</li>
<li>Satıcı faturası satırından mali boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Aşağıdaki koşullarla vergi:
<ul>
<li>Genel muhasebe parametreleri sayfasında ABD vergilendirme kurallarını uygula seçeneği seçili değil.</li>
<li>Satış vergi grupları sayfasında Satış vergi grubu için vergi alanını kullan seçili değil.</li>
</ul></td>
<td><ol>
<li>Vergi tutarı düşülebilir ise, Genel muhasebe deftere nakil grupları sayfasındaki Satış vergisi alacakları alanı.</li>
<li>Vergi tutarı düşülebilir değilse, masraf için genişletilmiş fiyat veya muhasebe dağılımı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Satıcı faturası satırındaki masraf için genişletilmiş fiyat veya muhasebe dağılımlarından gelen mali boyutları kullanın.</li>
<li>Satıcı faturası satırından mali boyut değerlerini kullanın.</li>
<li>Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="even">
<td>Aşağıdaki koşullarla vergi:
<ul>
<li>Genel muhasebe parametreleri sayfasında ABD vergilendirme kurallarını uygula seçeneği seçili değil.</li>
<li>Satış vergi grupları sayfasında Satış vergi grubu için vergi alanını kullan seçili.</li>
</ul></td>
<td><ol>
<li>Vergi tutarı düşülebilir ise, Genel muhasebe deftere nakil grupları sayfasındaki Satış vergisi alacakları alanı.</li>
<li>Vergi tutarı düşülebilir değilse, Genel muhasebe deftere nakil grupları sayfasındaki Kullanım vergisi gideri alanı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Satıcı faturası satırındaki masraf için genişletilmiş fiyat veya muhasebe dağılımlarından gelen mali boyutları kullanın.</li>
<li>Satıcı faturası satırından mali boyut değerlerini kullanın.</li>
<li>Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Masraf başlığı</td>
<td><ol>
<li>Masraflar kodu formundaki borç Türü alanında Genel muhasebe seçili ise, Masraflar kodu sayfasındaki borç Hesabı alanı.</li>
<li>Masraflar kodu formundaki borç Türü alanında Müşteri/Satıcı seçili ise, Masraflar kodu sayfasındaki kredi Hesabı alanı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</li>
<li>Satıcı faturası başlığından gelen mali boyut varsayılan şablon değerlerini kullanın.</li>
<li>Satıcı faturası satırından mali boyut değerlerini kullanın.</li>
<li>Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
<tr class="even">
<td>Başlık iskontosu</td>
<td><ol>
<li>Otomatik hareketler sayfasındaki Hesaplar içindeki Satıcı faturası iskontosu deftere nakil türü için Ana muhasebe alanı.</li>
</ol></td>
<td><ol>
<li>Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</li>
<li>Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</li>
<li>Satıcı faturası satırından mali boyut değerlerini kullanın.</li>
<li>Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a>Vergileri dağıtma
------------------

Vergiler için muhasebe dağılımları, vergiler hesaplanana dek oluşturulamaz. Satış vergilerini hesaplamak için Satıcı faturası sayfasında aşağıdaki görevleri tamamlamanız gerekir:
-   Fatura toplamını görüntüleyin.
-   Satış vergisini görüntüleyin.
-   Yardımcı defter günlüğünü görüntüleyin.
-   Komple satıcı faturası için muhasebe dağılımlarını görüntüleyin.
-   Satıcı faturasını beklemeye alın.
-   Satıcı faturasını deftere nakledin.

## <a name="subledger-journals-for-vendor-invoices"></a>Satıcı faturaları için muavin defteri günlükleri
Bir satıcı faturasını deftere nakletmeden önce, faturanın doğru hesaplara nakledildiğini teyit etmek için, borçlar ve alacaklar dahil, faturanın tüm muhasebe girdisini görebilirsiniz. Bu tam görünümün muavin defteri günlük hesap girişi olarak adlandırılır. 

Satıcı faturasını günlüğe geçirmeden önce önizlemesini görüntülediğinizde muavin defteri günlük girdisi yanlış ise, muavin defteri günlük girdisi değiştiremezsiniz. Bunun yerine, hesap dağılımlarını veya deftere nakil profilini değiştirmeniz gerekir. Hesap dağıtımları muhasebe girişi, Borç veya alacak bir tarafı tanımlamak için kullanılır. Mahsup eden muavin defteri günlüğü hesabı girişi, satıcı hesabından veya vergi gibi deftere nakil profilleri kullanılarak oluşturulabilir.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]