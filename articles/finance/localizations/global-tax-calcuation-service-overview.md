---
title: Vergi Hesaplamaya genel bakış
description: Bu makalede, Vergi Hesaplama özelliğinin tüm kapsamı ve özellikleri açıklanmaktadır.
author: EricWangChen
ms.date: 09/08/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: a193db82b2b079c1e10fbfb6bfde7aa43b18bc4a
ms.sourcegitcommit: dbb997f252377b8884674edd95e66caf8d817816
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/10/2022
ms.locfileid: "9465179"
---
# <a name="tax-calculation-overview"></a>Vergi Hesaplamaya genel bakış

[!include [banner](../includes/banner.md)]

Vergi Hesaplama, Global Tax Engine'in vergi belirleme ve hesaplama sürecini otomatikleştirmesini ve basitleştirmesini sağlayan, aşırı ölçeklenebilir çok kiracılı bir servistir. Tax Engine tam olarak konfigüre edilebilir. Konfigüre edilebilecek öğeler vergilendirilebilir veri modeli, vergi kodu, vergi uygulanabilirlik matrisi ve vergi hesaplama formülü ile sınırlı değildir. Tax Engine Microsoft Azure çekirdek hizmetler platformunda çalışır ve modern teknoloji ve artan ölçeklenebilirlik sunar.

Vergi Hesaplama, Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile tümleşiktir. Sonuç olarak, Dynamics 365 Project Operations, Dynamics 365 Commerce ve diğer birinci taraf ile üçüncü taraf uygulamaları ile de bütünleşir.

> [!IMPORTANT]
> Vergi Hesaplama hizmetini etkinleştirdiğinizde ilgili veriler üzerindeki bazı işlemler, servis verilerinizi barındıran veri merkezinden farklı bir veri merkezinde gerçekleştirilebilir. Vergi Hesaplama hizmetini etkinleştirmeden önce [Hükümler ve Koşullar](https://go.microsoft.com/fwlink/?linkid=2156043)'ı inceleyin. Gizliliğiniz bizim için önemlidir. Daha fazla bilgi için [Gizlilik Bildirimimizi](https://go.microsoft.com/fwlink/?LinkId=521839) okuyun.

Vergi Hesaplama, artan ölçeklenebilirlik sağlayan ve aşağıdaki görevleri gerçekleştirmenize yardımcı olabilecek mikro hizmet tabanlı bir vergi altyapısıdır:

- Gelişmiş bir belirleme mekanizması aracılığıyla doğru satış vergisi grubunu, madde satış vergisi grubunu ve vergi kodlarını otomatik olarak belirleyin.
- Tek bir tüzel kişilikte birden fazla vergi kayıt numarasını destekleyin ve vergiye tabi hareketlerin doğru vergi kayıt numarasını otomatik olarak belirleyin.
- Transfer emirleri için vergi belirleme, hesaplama, deftere nakletme ve kapatma desteği.
- Özel iş gereksinimleriniz için yapılandırılabilir vergi hesaplama formülleri ve koşullar tanımlayın.
- Bakım çabalarını en aza indirmek ve hataları önlemek için vergi belirleme ve hesaplama çözümünü tüzel kişilikler arasında paylaşın.
- Müşteri ve satıcıların vergi kayıt numaralarını belirleme desteği.
- Liste kodu belirleme desteği.
- Vergi dairesi düzeyinde vergi hesaplama parametreleri desteği.

Vergi Hesaplama'yı kullanmak için Microsoft Dynamics Lifecycle Services uygulamasındaki projenizden Vergi Hesaplama eklentisini yükleyin. Ardından [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) uygulamasındaki kurulumu tamamlayın ve Finance ve Supply Chain Management uygulamalarında Vergi Hesaplaması'nı etkinleştirin. Daha fazla bilgi için bkz. [Vergi hizmetini kullanmaya başlama](global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Kullanılabilirlik

Vergi Hesaplama, 10.0.21 sürümünden itibaren tüm müşteriler tarafından genel olarak üretim ortamlarında kullanılabilir.

Yeni özellikler sunulmaya devam edecek. Desteklenen özelliklerin kapsam bilgilerini öğrenmek için en güncel sürüm planını sık sık kontrol edin.

Vergi Hesaplama aşağıdaki Azure bölgelerinde dağıtılır. Müşteri gereksinimlerine göre daha fazla Azure bölgesi eklenecektir.

- Asya Pasifik
- Avustralya
- Brezilya
- Kanada
- Avrupa
- Fransa
- Hindistan
- Japonya
- Güney Afrika
- İsviçre
- Birleşik Arap Emirlikleri
- Birleşik Krallık
- Amerika Birleşik Devletleri

> [!NOTE]
> Vergi Hesaplama, Dynamics AX 2012 gibi Dynamics 365'in önceki sürümlerini veya Dynamics 365'in şirket içi dağıtımlarını desteklemez.

## <a name="versions"></a>Sürümler
Vergi hesaplama yapılandırmanızı, Finance veya Supply Chain Management sürümünüzle eşleşen sürümle içeri aktarmanız ve ayarlamanız önerilir.

| Finance veya Supply Chain Management sürümü | Vergi yapılandırması sürümü               |
| --------------- | --------------------------------------- |
| 10.0.30         | Vergi Hesaplama Yapılandırması 40.55.239 |
| 10.0.29         | Vergi Hesaplama Yapılandırması 40.55.236 |
| 10.0.28         | Vergi Hesaplama Yapılandırması 40.54.234 |
| 10.0.27         | Vergi Hesaplama Yapılandırması 40.54.234 |


## <a name="data-flow"></a>Veri akışı

Vergi Hesaplama için veri akışı işleminin bir özetini burada bulabilirsiniz. 

1. RCS'de vergilendirilebilir belge modeli yapılandırmalarını ve model eşleme yapılandırmalarını görüntüleyin ve içeri aktarın. Gelişmiş bir senaryo için yapılandırmaları genişletmeniz gerekiyorsa bkz. [Vergi yapılandırmalarına veri alanları ekleme](tax-service-add-data-fields-tax-configurations.md).
2. RCS'de vergi özellikleri oluşturun veya vergi özelliklerini koruyun. Vergi oranlarını ve vergi uygulanabilirlik kurallarını yönetmek için vergi özelliklerini kullanabilirsiniz.
3. Vergi özelliği kurulumu tamamlandıktan sonra vergi yapılandırmalarını ve vergi özelliklerini RCS'den Genel depoya yayımlayın.
4. Finance'te, belirli bir tüzel kişilik için hangi vergi özelliği kurulumu sürümünün kullanılacağını seçin.
5. Finance ve Supply Chain Management uygulamalarında hareketleri her zamanki gibi yürütün. Vergi Hesaplaması gerektiğinde istemci bilgileri satış siparişi veya satınalma siparişi gibi hareketten toplar ve yük olarak paketler. Daha sonra verginin hesaplanması için bir istek gönderilir.
6. Vergi hesaplama isteği istemciden alınır ve hesaplama tamamlanır. Vergi sonucu daha sonra istemciye döndürülür.
7. Dynamics 365 istemcisi vergi sonucunu alır ve vergi hesaplama sonucunu bir satış vergisi sayfasında sunar.

## <a name="supported-transactions"></a>Desteklenen işlemler

Vergi Hesaplama, hareketlere göre etkinleştirilebilir. 

Aşağıdaki tabloda, ilgili sürümde desteklenen işlemler listelenmektedir.

| Sürüm | Hareketler |
|---------|--------------|
| 10.0.29 | Periyodik günlükler |
| 10.0.28 | Satıcı ödeme günlüğü<br> Müşteri ödeme günlüğü | 
| 10.0.26 | Yevmiye defterleri<br> Satıcı fatura günlüğü |
| 10.0.23 | Serbest metin faturası |
| 10.0.21| Satış<br><ul><li>Satış teklifi</li><li>Satış siparişi</li><li>Onay</li><li>Malzeme çekme listesi</li><li>Sevk irsaliyesi</li><li>Satış faturası</li><li>Alacak dekontu</li><li>Sipariş iadesi</li><li>Başlık sair masrafları</li><li>Satır sair masrafları</li></ul>Satınalma<br><ul><li>Satın alma siparişi</li><li>Onay</li><li>Giriş listesi</li><li>Ürün girişi</li><li>Satınalma faturası</li><li>Başlık sair masrafları</li><li>Satır sair masrafları</li><li>Alacak dekontu</li><li>Sipariş iadesi</li><li>Satınalma talebi</li><li>Satın alma talebi satır sair masrafı</li><li>Teklif talebi</li><li>Teklif talebi başlık sair masrafı</li><li>Teklif talebi satır sair masrafı</li></ul>Stok<ul><li>Transfer emri - sevk</li><li>Transfer emri - al</li></ul>|

## <a name="supported-countriesregions"></a>Desteklenen ülkeler/bölgeler

Vergi Hesaplaması, desteklenen yerelleştirme özellikleriyle çalıştırılabilir. Aşağıdaki tabloda, tüzel kişiliğin birincil adresi için ülkeler/bölgeler listelenmektedir.

| Sürüm | Ülke/bölge |
|---------|----------------|
| 10.0.26 | - Çin <br>- Çek Cumhuriyeti<br>- İspanya |
| 10.0.24 | Meksika |
| 10.0.23 | - Tayland <br>- Japonya <br>- Malezya <br>- Singapur |
| 10.0.22 | - Avustralya<br>- Bahreyn <br>- Kanada<br>- Mısır <br>- Hong Kong ÖİB <br>- Kuveyt <br>- Yeni Zelanda <br>- Umman <br>- Katar <br>- Suudi Arabistan Arapçası <br>- Güney Afrika <br>- Birleşik Arap Emirlikleri |
| 10.0.21 | - Avusturya <br>- Belçika <br>- Danimarka <br>- Estonya <br>- Finlandiya <br>- Fransa <br>- Almanya <br>- Macaristan <br>- İzlanda <br>- İrlanda <br>- İtalya <br>- Letonya <br>- Litvanya <br>- Hollanda <br>- Norveç <br>- Polonya <br>- İsveç <br>- İsviçre <br>- Birleşik Krallık <br>- ABD |

Microsoft tarafından yerelleştirilmemiş herhangi bir ülke/bölge için vergi hesaplaması diğer global özelliklerle de etkinleştirilebilir ve çalıştırılabilir.

## <a name="related-resources"></a>İlgili kaynaklar

[Vergi hizmetini kullanmaya başlama](./global-get-started-with-tax-calculation-service.md)

[Çoklu KDV kayıt numarası](./emea-multiple-vat-registration-numbers.md)

[Transfer emri için vergi özelliği desteği](./tasks/tax-feature-support-for-transfer-order.md)

[Vergi hizmetinde uzantı oluşturma](./tax-service-add-data-fields-tax-integration-by-extension.md)
