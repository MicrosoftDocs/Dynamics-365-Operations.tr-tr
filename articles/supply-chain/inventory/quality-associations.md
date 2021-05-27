---
title: Kalite ilişkileri
description: Bu konu, satış, satınalma ve üretim süreçleriniz ile ilgili kalite emirlerini otomatik olarak oluşturmak için Microsoft Dynamics 365 Supply Chain Management'ta kalite ilişkilendirmelerini nasıl kullanabileceğinizi açıklamaktadır.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c6fab1b89b7e58d9e443c27da03a6b13afcc9c6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022336"
---
# <a name="quality-associations"></a>Kalite ilişkileri

[!include [banner](../includes/banner.md)]

Bu konu, satış, satınalma ve üretim süreçleriniz ile ilgili kalite emirlerini otomatik olarak oluşturmak için Microsoft Dynamics 365 Supply Chain Management'ta kalite ilişkilendirmelerini nasıl kullanabileceğinizi açıklamaktadır.

Bir kalite ilişkisi oluşturulan bir kalite emri için aşağıdaki tüm bilgileri tanımlar:

- Hareket olayı
- Öğeler üzerinde gerçekleştirilmesi gereken test dizileri
- Kabul edilebilir kalite düzeyi (AQL)
- Örnekleme planı

Kalite emirlerinin otomatik olarak oluşturulmasını gerektiren iş işlemindeki her farklılık için bir kalite eşleştirmesi tanımlamanız gerekmektedir. Örneğin, satınalma siparişleri, karantina siparişleri, satış siparişleri ve üretim emirleri için iş süreçlerinde bir kalite emri oluşturulabilir.

## <a name="working-with-quality-associations"></a>Kalite ilişkileri ile çalışmak

Kalite ilişkisini kullanan iş süreci, satınalma siparişleri, satış siparişleri veya üretim emirleri gibi çeşitli kaynak belgelere ilişkili olabilir.

Her kalite bağlantısı kaydı oluşturulan kalite emirlerine geçerli olacak testler kümesini, AQL'yi ve örnek alma planını da tanımlamaktadır. Bir iş sürecindeki her değişim için bir kalite ilişkisi kaydı tanımlamanız gerekir. Örneğin, bir satınalma siparişi ürün alış irsaliyesi güncelleştirildiğinde, kalite emri oluşturacak bir kalite ilişkisi ayarlayabilirsiniz. Yürütme planının kurulumuna bağlı olarak, tetikleme işleminin kendisi açık bir kalite emri olduğunda bloke edilebilir. Ayrıca, satınalma siparişi faturalama gibi sonraki işlemler bloke edilebilir.

> [!NOTE]
> Açık kalite emirleri olduğunda, stok miktarlarının çıkarılması otomatik olarak engellenir. **Madde örnekleri** sayfasında bulunan **Tam engelleme** alanı ayarlarına bağlı olarak, miktar kalite emrindeki miktardır ya da kaynak belge satırındaki miktardır. Daha fazla bilgi için bkz. [Kalite yönetimi madde örnekleme](quality-item-sampling.md).

Bir iş süreci için, kalite ilişkisi kaydı, kalite emrinin oluşturulduğu olay ve koşulları tanımlar. Koşullar bir siteye veya bir tüzel kişiliğe özel olabilir. Bozucu testler içeren bir kalite emri yalnızca olay için eldeki stok bulunması durumunda oluşturulabilir.

Kalite ilişkilendirmeleriyle çalışmak için **Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite ilişkilendirmeleri**'ne gidin. Aşağıdaki örnekler, her iş sürecindeki değişiklikler için bir kalite bağlantısını tanımlamayı açıklar. Her örnek için, aşağıdaki tablo kalite ilişki kaydındaki olayları ve durumları özetler.

<table>
<thead>
<tr>
<th>Referans türü</th>
<th>Olay türü</th>
<th>Yürütme</th>
<th>Olay durdurma</th>
<th>Belge başvurusu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stok</td>
<td>Geçerli değil</td>
<td>Geçerli değil</td>
<td>Yok</td>
<td>Tümü</td>
</tr>
<tr>
<td rowspan="7">Satışlar</td>
<td rowspan="4">Malzeme çekme işlemi planlandı</td>
<td rowspan="4">Önce</td>
<td>Yok</td>
<td rowspan="22">Belirli Kimlik, Grup veya Yalnızca tümü</td>
</tr>
<tr>
<td>Malzeme çekme işlemi</td>
</tr>
<tr>
<td>Sevk irsaliyesi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="3">Sevk irsaliyesi</td>
<td rowspan="3">Önce</td>
<td>Yok</td>
</tr>
<tr>
<td>Sevk irsaliyesi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="15">Satınalma</td>
<td rowspan="7">Giriş listesi</td>
<td rowspan="4">Önce</td>
<td>Yok</td>
</tr>
<tr>
<td>Giriş listesi</td>
</tr>
<tr>
<td>Ürün girişi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="3">Sonra</td>
<td>Yok</td>
</tr>
<tr>
<td>Ürün girişi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="3">Kayıt</td>
<td rowspan="3">Geçerli değil</td>
<td>Yok</td>
</tr>
<tr>
<td>Ürün girişi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="5">Ürün girişi</td>
<td rowspan="3">Önce</td>
<td>Yok</td>
</tr>
<tr>
<td>Ürün girişi</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="2">Sonra</td>
<td>Yok</td>
</tr>
<tr>
<td>Fatura</td>
</tr>
<tr>
<td rowspan="8">Üretim</td>
<td rowspan="3">Kayıt</td>
<td rowspan="3">Geçerli değil</td>
<td>Yok</td>
<td rowspan="12">Tümü</td>
</tr>
<tr>
<td>Tamamlandı bildirimi</td>
</tr>
<tr>
<td>Bitir</td>
</tr>
<tr>
<td rowspan="5">Tamamlandı bildirimi</td>
<td rowspan="3">Önce</td>
<td>Yok</td>
</tr>
<tr>
<td>Tamamlandı bildirimi</td>
</tr>
<tr>
<td>Bitir</td>
</tr>
<tr>
<td rowspan="2">Sonra</td>
<td>Yok</td>
</tr>
<tr>
<td>Bitir</td>
</tr>
<tr>
<td rowspan="4">Karantina</td>
<td rowspan="3">Tamamlandı bildirimi</td>
<td rowspan="2">Önce</td>
<td>Tamamlandı bildirimi</td>
</tr>
<tr>
<td>Bitir</td>
</tr>
<tr>
<td>Sonra</td>
<td>Bitir</td>
</tr>
<tr>
<td>Bitir</td>
<td>Önce</td>
<td>Bitir</td>
</tr>
<tr>
<td rowspan="3">Rota operasyonu</td>
<td rowspan="3">Tamamlandı bildirimi</td>
<td rowspan="2">Önce</td>
<td>Hiçbiri</td>
<td rowspan="3">Belirli Kimlik, Grup veya Tümü ve Kaynağa özel, Grup veya Tümü</td>
</tr>
<tr>
<td>Tamamlandı bildirimi</td>
</tr>
<tr>
<td>Sonra</td>
<td>Hiçbiri</td>
</tr>
<tr>
<td rowspan="3">Ortak ürün üretimi</td>
<td>Kayıt</td>
<td>Geçerli değil</td>
<td rowspan="3">Hiçbiri</td>
<td rowspan="3">Tümü</td>
</tr>
<tr>
<td rowspan="2">Tamamlandı bildirimi</td>
<td>Önce</td>
</tr>
<tr>
<td>Sonra</td>
</tr>
</tbody>
</table>

> [!NOTE]
> *Ambar işlemleri için kalite yönetimi* özelliği, **Olay Türü** alanı *Tamamlandı olarak bildir*, **Yürütme** alanı *Sonra* olarak ayarlanmış olan üretim ve **Olay türü** alanı *Kayıt* olarak ayarlanmış satınalmalar için kalite emri işleme yetenekleri ekler. Daha fazla bilgi için bkz. [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md).

Aşağıdaki tabloda belirli türde işlemler için kalite emirlerinin nasıl oluşturulabileceği hakkında daha fazla bilgi sağlar.

<div class="tableSection">
<table>
<thead>
<tr>
<th>İşleme türü</th>
<th>Kalite emirlerinin ne zaman otomatik olarak oluşturulabileceği</th>
<th>Bozucu sınama yapılması gerekirse kalite emirlerinin ne zaman oluşturulabileceği</th>
<th>Koşul bilgisi</th>
<th>El ile oluşturma bilgisi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Satın alma siparişi</td>
<td>Alınan malzeme için ürün girişi ya da giriş listesi nakledildikten önce veya sonra.</td>
<td>Alınan malzeme için ürün girişi nakledildikten sonra, çünkü malzemenin bozucu test için mevcut olması gerekmektedir.</td>
<td>Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir satınalma siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Karantina emri</td>
<td>Karantina siparişi tamamlandı veya sona erdi olarak bildirildikten önce veya sonra.</td>
<td>Yıkıcı testler gerektiren kalite emirleri oluşturulamaz. Karantina siparişi işlevinin, yok edilen malzemenin elden çıkarılmasını üstleneceği kabul edilir.</td>
<td>Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir karantina siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Satış siparişi</td>
<td>Bir zamanlanmış malzeme çekme işlem veya sevk irsaliyesi güncelleştirmesi sevk maddeler için önce</td>
<td>Herhangi bir adımda</td>
<td>Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir satış siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Üretim emri</td>
<td>Üretim emri için bitmiş miktar rapor edildikten önce veya sonra</td>
<td>Üretim emri için bitmiş miktar rapor edildikten sonra</td>
<td>Kalite emri gereksinimi özel bir tesisi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir üretim emrine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Bir rota operasyonuna sahip olan üretim emri</td>
<td>Bir operasyon için bir rapor sona erdikten önce veya sonra</td>
<td>Son operasyon için raporlama üretimi bittikten sonra.</td>
<td>Kalite emri gereksinimi özel bir tesisi, maddeyi veya operasyon kaynağı ya da bunların bir birleşimini yansıtabilir.</td>
<td>Bir rota operasyonu gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</td>
</tr>
<tr>
<td>Stok</td>
<td>Bir kalite emri, transfer emri hareketleri veya bir stok günlüğünde bir hareket için otomatik olarak oluşturulamaz.</td>
<td></td>
<td></td>
<td>Bir kalite emrinin bir maddenin stok miktarı için el ile oluşturulması gerekir. Fiziksel eldeki stok gereklidir.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Kalite emirlerinin otomatik oluşturulmasına ilişkin örnekler

### <a name="purchasing"></a>Satınalma

Satınalmada, **Kalite ilişkilendirmeleri** sayfasında **Olay türü** alanını *Ürün girişi* ve **Yürütme** alanını *Sonra* olarak ayarlarsanız aşağıdaki sonuçları elde edersiniz:

- **Güncelleştirilen miktar başına** seçeneği *Evet* olarak ayarlanmışsa, madde örneklemesindeki teslim alınan miktar ve ayarlar temel alınarak satınalma siparişiyle ilgili her giriş için bir kalite emri oluşturulur. Satınalma siparişine göre bir miktar her teslim alındığında, yeni teslim alınan miktar temel alınarak geçerli kalite emirleri oluşturulur.
- **Güncelleştirilen miktar başına** seçeneği *Hayır* olarak ayarlanmışsa, teslim alınan miktar ve ayarlar temel alınarak satınalma siparişiyle ilgili ilk giriş için bir kalite emri oluşturulur. Ayrıca, izleme boyutlarına bağlı olarak kalan miktar temel alınarak bir veya daha fazla kalite emri oluşturulur. Satınalma siparişiyle ilgili sonraki girişler için kalite emirleri oluşturulmaz.

### <a name="production"></a>Üretim

Üretimde, **Kalite ilişkilendirmeleri** sayfasında **Olay türü** alanını *Tamamlandı olarak bildir* ve **Yürütme** alanını *Sonra* olarak ayarlarsanız aşağıdaki sonuçları elde edersiniz:

- **Güncelleştirilen miktar başına** seçeneği *Evet* olarak ayarlanmışsa, madde örneklemesindeki her tamamlanan miktar için bir kalite emri oluşturulur. Üretim emrine göre bir miktar her tamamlandı olarak bildirildiğinde, yeni tamamlanan miktar temel alınarak geçerli kalite emirleri oluşturulur. Bu oluşturma mantığı satın alma ile tutarlıdır.
- **Güncelleştirilen miktar başına** seçeneği *Hayır* olarak ayarlanmışsa, tamamlanan miktar temel alınarak bir miktar ilk kez tamamlandı olarak bildirildiğinde bir kalite emri oluşturulur. Ayrıca, madde örneklemesinin izleme boyutlarına bağlı olarak kalan miktar temel alınarak bir veya daha fazla kalite emri oluşturulur. Sonraki tamamlanan miktarlar için kalite emirleri oluşturulmaz.

<table>
<thead>
<tr>
<th>Kalite belirtimi</th>
<th>Güncelleştirilen miktar başına</th>
<th>İzleme boyutu başına</th>
<th>Sonuç</th>
</tr>
</thead>
<tbody>
<tr>
<td>Yüzde: %10</td>
<td>Evet</td>
<td>
<p>Toplu iş numarası: Hayır</p>
<p>Seri numarası: Hayır</p>
</td>
<td>
<p>Sipariş miktarı: 100</p>
<ol>
<li>30 için tamamlandı olarak bildir
<ul>
<li>3 için (30'un %10'u) için kalite emri 1</li>
</ul>
</li>
<li>70 için tamamlandı olarak bildir
<ul>
<li>7 (kalan sipariş miktarının %10'u; bu durumda 70'e eşittir) için kalite emri 2</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Sabit miktar: 1</td>
<td>No</td>
<td>
<p>Toplu iş numarası: Hayır</p>
<p>Seri numarası: Hayır</p>
</td>
<td>Sipariş miktarı: 100
<ol>
<li>30 için tamamlandı olarak bildir
<ul>
<li>1 için kalite emri 1 (sabit değeri 1 olan ilk tamamlandı bildirimi miktarı için)</li>
<li>1 için kalite emri 2 (sabit değeri hala 1 olan kalan miktar için)</li>
</ul>
</li>
<li>10 için tamamlandı olarak bildir
<ul>
<li>Kalite emri oluşturulmaz.</li>
</ul>
</li>
<li>60 için tamamlandı olarak bildir
<ul>
<li>Kalite emri oluşturulmaz.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Sabit miktar: 1</td>
<td>Evet</td>
<td>
<p>Toplu iş numarası: Evet</p>
<p>Seri numarası: Evet</p>
</td>
<td>
<p>Sipariş miktarı: 10</p>
<ol>
<li>3 için tamamlanmış haliyle rapor: toplu iş numarası b1, seri numarası s için 1; toplu iş numarası b2, seri numarası s2 için 1 ve toplu iş numarası b3, seri numarası s3 için 1
<ul>
<li>Toplu iş b1, seri s1'in 1'i için kalite emri 1</li>
<li>Toplu iş b2, seri s2'nin 1'i için kalite emri 2</li>
<li>Toplu iş b3, seri s3'ün 1'i için kalite emri 3</li>
</ul>
</li>
<li>2 için tamamlanmış haliyle rapor: toplu iş numarası b4, seri numarası s4 için 1 ve toplu iş numarası b5, seri numarası s5 için 1
<ul>
<li>Toplu iş b4, seri s4'ün 1'i için kalite emri 4</li>
<li>Toplu iş b5, seri s5'in 1'i için kalite emri 5</li>
</ul>
</li>
</ol>
<p><strong>Not:</strong> Toplu iş yeniden kullanılabilir.</p>
</td>
</tr>
<tr>
<td>Sabit miktar: 2</td>
<td>No</td>
<td>
<p>Toplu iş numarası: Evet</p>
<p>Seri numarası: Evet</p>
</td>
<td>
<p>Sipariş miktarı: 10</p>
<ol>
<li>4 için tamamlanmış haliyle rapor: toplu iş numarası b1, seri numarası s için 1; toplu iş numarası b2, seri numarası s2 için 1 ve toplu iş numarası b3, seri numarası s3 için 1 ve toplu iş numarası b4, seri numarası s4 için 1
<ul>
<li>Toplu iş b1, seri s1'in 1'i için kalite emri 1</li>
<li>Toplu iş b2, seri s2'nin 1'i için kalite emri 2</li>
<li>Toplu iş b3, seri s3'ün 1'i için kalite emri 3</li>
<li>Toplu iş b4, seri s4'ün 1'i için kalite emri 4</li>
</ul>
<ul>
<li>Bir toplu iş numarası ve bir seri numarasına referans olmadan, 2 için kalite emri 5.</li>
</ul>
</li>
<li>6 için tamamlanmış haliyle: toplu iş numarası b5, seri numarası s5 için 1; toplu iş numarası b6, seri numarası s6 için 1; toplu iş numarası b7, seri numara s7 için 1; toplu iş numarası b8, seri numarası s8 için 1; toplu iş numarası b9, seri numarası s9 için 1 ve toplu iş numarası b10, seri numarası s10 için 1
<ul>
<li>Kalite emri oluşturulmaz.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalite yönetimi işlemleri](quality-management-processes.md)
- [Kalite ve uygunsuzluk yönetimini etkinleştirme](enable-quality-management.md)
- [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
