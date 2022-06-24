---
title: Vergi Hesaplamaya genel bakış
description: Bu makalede, Vergi Hesaplama özelliğinin tüm kapsamı ve özellikleri açıklanmaktadır.
author: wangchen
ms.date: 03/02/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c9511643806a2201b3379dec9bbca01a8ccbcdc3
ms.sourcegitcommit: 58af7348be9ce60a86a111ede42a7fc5b2b77708
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2022
ms.locfileid: "8941744"
---
# <a name="tax-calculation-overview"></a>Vergi Hesaplamaya genel bakış

[!include [banner](../includes/banner.md)]

Vergi Hesaplama, Global Tax Engine'in vergi belirleme ve hesaplama sürecini otomatikleştirmesini ve basitleştirmesini sağlayan, aşırı ölçeklenebilir çok kiracılı bir servistir. Tax Engine tam olarak konfigüre edilebilir. Konfigüre edilebilecek öğeler vergilendirilebilir veri modeli, vergi kodu, vergi uygulanabilirlik matrisi ve vergi hesaplama formülü ile sınırlı değildir. Tax Engine Microsoft Azure çekirdek hizmetler platformunda çalışır ve modern teknoloji ve artan ölçeklenebilirlik sunar.

Vergi Hesaplama, Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile tümleşiktir. Sonuç olarak, Dynamics 365 Project Operations, Dynamics 365 Commerce ve diğer birinci taraf ile üçüncü taraf uygulamaları ile de bütünleşir.

> [!IMPORTANT]
> Vergi Hesaplama hizmetini etkinleştirdiğinizde ilgili veriler üzerindeki bazı işlemler, servis verilerinizi barındıran veri merkezinden farklı bir veri merkezinde gerçekleştirilebilir. Vergi Hesaplama hizmetini etkinleştirmeden önce [Hükümler ve Koşullar](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md)'ı inceleyin. Gizliliğiniz bizim için önemlidir. Daha fazla bilgi için [Gizlilik Bildirimimizi](https://go.microsoft.com/fwlink/?LinkId=521839) okuyun.

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
- Kanada
- Avrupa
- Japonya
- İsviçre
- Birleşik Krallık
- Amerika Birleşik Devletleri

> [!NOTE]
> Vergi Hesaplama, Dynamics AX 2012 gibi Dynamics 365'in önceki sürümlerini veya Dynamics 365'in şirket içi dağıtımlarını desteklemez.

## <a name="versions"></a>Sürümler
Vergi hesaplama yapılandırmanızı, Finance veya Supply Chain Management sürümünüzle eşleşen sürümle içeri aktarmanız ve ayarlamanız önerilir.

| Finance veya Supply Chain Management sürümü | Vergi yapılandırması sürümü               |
| --------------- | --------------------------------------- |
| 10.0.18         | Vergi Yapılandırması - Avrupa 30.12.82     |
| 10.0.19         | Vergi Hesaplama Yapılandırması 36.38.193 |
| 10.0.20         | Vergi Hesaplama Yapılandırması 40.43.208 |
| 10.0.21         | Vergi Hesaplama Yapılandırması 40.48.215 |
| 10.0.22         | Vergi Hesaplama Yapılandırması 40.48.215 |
| 10.0.23         | Vergi Hesaplama Yapılandırması 40.50.221 |
| 10.0.24         | Vergi Hesaplama Yapılandırması 40.50.225 |
| 10.0.25         | Vergi Hesaplama Yapılandırması 40.50.225 |
| 10.0.26         | Vergi Hesaplama Yapılandırması 40.54.234 |
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

Aşağıdaki hareketler sürüm 10.0.21'de desteklenmektedir: 

- Satışlar

    - Satış teklifi
    - Satış siparişi
    - Onay
    - Malzeme çekme listesi
    - Sevk irsaliyesi
    - Satış faturası
    - Alacak dekontu
    - Sipariş iadesi
    - Başlık sair masrafları
    - Satır sair masrafları

- Satınalma

    - Satın alma siparişi
    - Onay
    - Giriş listesi
    - Ürün girişi
    - Satınalma faturası
    - Başlık sair masrafları
    - Satır sair masrafları
    - Alacak dekontu
    - Sipariş iadesi
    - Satınalma talebi
    - Satın alma talebi satır sair masrafı
    - Teklif talebi
    - Teklif talebi başlık sair masrafı
    - Teklif talebi satır sair masrafı

- Stok

    - Transfer emri - sevk
    - Transfer emri - al

Aşağıdaki hareketler sürüm 10.0.23'de desteklenmektedir: 

- Serbest metin faturası

Aşağıdaki hareketler sürüm 10.0.26'de desteklenmektedir: 

- Yevmiye defterleri
- Satıcı fatura günlüğü

Aşağıdaki hareketler sürüm 10.0.28'de desteklenmektedir: 

- Satıcı ödeme günlüğü
- Müşteri ödeme günlüğü

## <a name="supported-countriesregions"></a>Desteklenen ülkeler/bölgeler

Vergi Hesaplama, tüzel kişilik tarafından etkinleştirilebilir. 

Tüzel kişiliğin birincil adresi için aşağıdaki ülkeler/bölgeler 10.0.21 sürümünde desteklenir:

- Avusturya
- Belçika
- Danimarka
- Estonya
- Finlandiya
- Fransa
- Almanya
- Macaristan
- İzlanda
- İrlanda
- İtalya
- Letonya
- Litvanya
- Hollanda
- Norveç
- Polonya
- İsveç
- İsviçre
- Birleşik Krallık
- Amerika Birleşik Devletleri

Tüzel kişiliğin birincil adresi için aşağıdaki ülkeler/bölgeler 10.0.22 sürümünde desteklenir:

- Avustralya
- Bahreyn
- Kanada
- Mısır
- Hong Kong Çin ÖİB
- Kuveyt
- Yeni Zelanda
- Umman
- Katar
- Suudi Arabistan
- Güney Afrika
- Birleşik Arap Emirlikleri

Tüzel kişiliğin birincil adresi için aşağıdaki ülkeler/bölgeler 10.0.23 sürümünde desteklenir:

- Tayland
- Japonya
- Malezya
- Singapur

Tüzel kişiliğin birincil adresi için aşağıdaki ülkeler/bölgeler 10.0.24 sürümünde desteklenir:

- Meksika

Tüzel kişiliğin birincil adresi için aşağıdaki ülkeler/bölgeler 10.0.26 sürümünde desteklenir:

- Çin
- Çek Cumhuriyeti
- İspanya

## <a name="related-resources"></a>İlgili kaynaklar

[Vergi hizmetini kullanmaya başlama](./global-get-started-with-tax-calculation-service.md)

[Çoklu KDV kayıt numarası](./emea-multiple-vat-registration-numbers.md)

[Transfer emri için vergi özelliği desteği](./tasks/tax-feature-support-for-transfer-order.md)

[Vergi hizmetinde uzantı oluşturma](./tax-service-add-data-fields-tax-integration-by-extension.md)
