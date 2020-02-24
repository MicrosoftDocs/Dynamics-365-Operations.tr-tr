---
title: Common Data Service varlıkları
description: Microsoft Dynamics 365 Human Resources, Common Data Service genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85dd95e8209fff28f214986f7960372db200351b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010911"
---
# <a name="common-data-service-entities"></a>Common Data Service varlıkları

Microsoft Dynamics 365 Human Resources, Common Data Service genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.

Common Data Service hakkında daha fazla bilgi için bkz. [Common Data Service nedir?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Aşağıdaki İnsan Kaynakları varlıkları Common Data Service'de kullanılabilir.

## <a name="benefit-entities"></a>Yarar varlıkları

**Kazanç Hesaplama Sıklığı**

| **Alanlar**        | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------------|---------------|--------------|----------------|
| Tanım       | Text          |              | X              |
| Sıklık denetimi | Seçenek kümesi    | X            | X              |
| Değiştirilemez      | İki seçenek   |              | X              |
| Dosya Adı              | Text          | X            | X              |


**Kazanç hesaplama oranı**

| **Alanlar**  | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------|---------------|--------------|----------------|
| Tanım | Text          |              | X              |
| Dosya Adı        | Text          | X            | X              |
| TierType    | Seçenek kümesi    | X            | X              |


**Kazanç hesaplama oranı ayrıntısı**

| **Alanlar**                             | **Veri türü**  | **Gerekli** | **Aranabilir** |
|----------------------------------------|----------------|--------------|----------------|
| Kazanç hesaplama oranı ayrıntı numarası | Text           | X            | X              |
| Hesaplama oranı kimliği                    | Arama         | X            | X              |
| Katkı Yöntemi                    | Seçenek Kümesi     | X            | X              |
| Yürürlüğe giriş                              | Yalnızca Tarih      | X            | X              |
| İşveren Katkısı                  | Ondalık sayısı |              | X              |
| Bitiş tarihi                             | Yalnızca Tarih      | X            | X              |
| WorkerDeduction                        | Ondalık sayısı |              | X              |


**Kazanç türü**

| **Alanlar**           | **Veri türü** | **Gerekli** | **Aranabilir** |
|----------------------|---------------|--------------|----------------|
| ConcurrentEnrollment | Seçenek kümesi    |              | X              |
| Tanım          | Text          |              | X              |
| Dosya Adı                 | Text          | X            | X              |
| PayrollCategory      | Seçenek kümesi    |              | X              |


**Kazanç planı**

| **Alanlar**                               | **Veri türü**  | **Gerekli** | **Aranabilir** |
|------------------------------------------|----------------|--------------|----------------|
| Arrear Sınır yöntemi                      | Seçenek kümesi     |              | X              |
| Kazanç Türü                             | Arama         | X            | X              |
| Katkı sınır yöntemi                | Seçenek kümesi     |              | X              |
| Katkı Yöntemi                      | Seçenek kümesi     |              | X              |
| Para Birimi                                 | Arama         |              | X              |
| Kesinti Önceliği                       | Tam sayı   |              | X              |
| Varsayılan Katkı Sınırı Tutarı        | Para Birimi       |              | X              |
| Varsayılan katkı sınırı miktarı (Taban) | Para Birimi       |              | X              |
| Varsayılan Katkı Sınırı Dönemi        | Seçenek kümesi     |              | X              |
| Varsayılan Kesinti Sınırı Tutarı           | Para Birimi       |              | X              |
| Varsayılan kesinti sınırı miktarı (Taban)    | Para Birimi       |              | X              |
| Varsayılan Kesinti Sınırı Dönemi           | Seçenek kümesi     |              | X              |
| Tanım                              | Text           |              | X              |
| Döviz Kuru                            | Ondalık sayısı |              | X              |
| Ek Bordro çalışması                | İki seçenek    |              | X              |
| Ekonomik Bakım Yasası bakımından bildirilebilir        | İki seçenek    |              | X              |
| Arrear oluşturuldu                      | İki seçenek    |              | X              |
| Brütleştirme                              | İki seçenek    |              | X              |
| Birincil                               | İki seçenek    |              | X              |
| Dosya Adı                                     | Text           | X            | X              |
| Bordro Etkisi                           | Seçenek kümesi     |              | X              |
| Emeklilik Türü                          | Seçenek kümesi     |              | X              |


**İstihdam varlığı**

| **Alanlar**                     | **Veri türü**  | **Gerekli** | **Aranabilir** |
|--------------------------------|----------------|--------------|----------------|
| Çalışanın ayarlanan başlama tarihi     | Tarih ve Saat  |              | X              |
| Şirket                        | Arama         | X            | X              |
| İşveren uyarı birimi tutarı | Ondalık sayısı |              | X              |
| Çalışan bildiri birimi        | Seçenek Kümesi     |              | X              |
| İş bitiş tarihi            | Tarih ve Saat  |              | X              |
| Çalışan sayısı              | Text           | X            | X              |
| İstihdam Başlama Tarihi          | Tarih ve Saat  |              | X              |
| Son Çalışma Tarihi              | Tarih ve Saat  |              | X              |
| Geçiş Tarihi                | Tarih ve Saat  |              | X              |
| Geçerlilik Başlangıcı                     | Tarih ve Saat  | X            | X              |
| Geçerlilik Bitişi                       | Tarih ve Saat  |              | X              |
| Çalışan                         | Arama         | X            | X              |
| Çalışan İlan Tutarı           | Ondalık sayısı |              | X              |
| Çalışanın Başlama Tarihi             | Tarih ve Saat  |              | X              |
| Çalışan Türü                    | Seçenek Kümesi     | X            | X              |
| Çalışan bildiri birimi          | Seçenek Kümesi     |              | X              |

## <a name="worker-entities"></a>Çalışan kişilikler

**Etnik köken**

| **Alanlar**         | **Veri türü** | **Gerekli** | **Aranabilir** |
|--------------------|---------------|--------------|----------------|
| Tanım        | Text          |              | X              |
| Etnik köken adı | Text          | X            | X              |


**Dil**

| **Alanlar**    | **Veri türü** | **Gerekli** | **Aranabilir** |
|---------------|---------------|--------------|----------------|
| Tanım   | Text          |              | X              |
| Dil adı | Text          | X            | X              |


**Gazilik durumu**

| **Alanlar**           | **Veri türü** | **Gerekli** | **Aranabilir** |
|----------------------|---------------|--------------|----------------|
| Tanım          | Text          |              | X              |
| Korunan Gazi | İki seçenek    |              | X              |
| Dil adı        | Text          | X            | X              |


**Çalışan**

| **Alanlar**                | **Veri türü** | **Gerekli** | **Aranabilir** |
|---------------------------|---------------|--------------|----------------|
| Doğum tarihi                 | Yalnızca Tarih     |              | X              |
| Tanım               | Text          |              | X              |
| E-posta adresi 1           | E-posta         |              | X              |
| E-posta adresi 2           | E-posta         |              | X              |
| Facebook Kimliği         | Text          |              | X              |
| Ad                | Text          |              | X              |
| Tam ad                 | Text          |              | X              |
| Cinsiyet                    | Seçenek Kümesi    |              | X              |
| Oluşturma                | Text          |              | X              |
| E-posta İletişimine İzin Verilir  | İki seçenek   |              | X              |
| Telefon İletişimine İzin Verilir  | İki seçenek   |              | X              |
| Soyadı                 | Text          |              | X              |
| LinkedIn Kimliği         | Text          |              | X              |
| Yönetici                   | Arama        |              | X              |
| İkinci Ad               | Text          |              | X              |
| Cep Telefonu              | Telefon         |              | X              |
| Office Graph Tanımlayıcısı   | Text          |              | X              |
| Birincil e-posta adresi     | E-posta         |              | X              |
| Birincil telefon         | Telefon         |              | X              |
| Meslek                | Text          |              | X              |
| Sosyal Ağ 1          | Seçenek Kümesi    |              | X              |
| Sosyal Ağ 2          | Seçenek Kümesi    |              | X              |
| Sosyal Ağ Kimliği 1 | Text          |              | X              |
| Sosyal Ağ Kimliği 2 | Text          |              | X              |
| Kaynak                    | Seçenek Kümesi    | X            | X              |
| Durum                    | Seçenek Kümesi    | X            | X              |
| Telefon 1               | Telefon         |              | X              |
| Telefon 2               | Telefon         |              | X              |
| Telefon 3               | Telefon         |              | X              |
| Twitter kimliği          | Text          |              | X              |
| Kullanıcı                      | Arama        |              | X              |
| Web Sitesi URL'si               | URL           |              | X              |
| Çalışan Sayısı             | Text          | X            | X              |
| Çalışan Türü               | Seçenek Kümesi    | X            | X              |
| Yomi Ad           | Text          |              | X              |
| Yomi Tam adı            | Text          |              | X              |
| Yomi Soyadı            | Text          |              | X              |
| Yomi İkinci ad          | Text          |              | X              |


**Çalışan adresi**

| **Alanlar**           | **Veri türü**  | **Gerekli** | **Aranabilir** |
|----------------------|----------------|--------------|----------------|
| Adres Numarası       | Text           | X            | X              |
| Adres Türü         | Seçenek Kümesi     | X            | X              |
| Şehir                 | Text           |              | X              |
| Ülke veya Bölge    | Text           |              | X              |
| İlçe               | Text           |              | X              |
| Faks                  | Telefon          |              | X              |
| Tercih edilen         | İki seçenek    |              | X              |
| Enlem             | Ondalık sayısı |              | X              |
| Satır 1               | Text           |              | X              |
| Satır 2               | Text           |              | X              |
| Satır 3               | Text           |              | X              |
| Boylam            | Ondalık sayısı |              | X              |
| Posta Kodu          | Text           |              | X              |
| Posta Kutusu      | Text           |              | X              |
| Sevkiyat Yöntemi Kodu | Tam sayı   |              | X              |
| İl veya İdari Bölge    | Text           |              | X              |
| Telefon 1          | Telefon          |              | X              |
| Telefon 2          | Telefon          |              | X              |
| Telefon 3          | Telefon          |              | X              |
| UPS Bölgesi             | Text           |              | X              |
| UTC Ofset           | Tam sayı   |              | X              |
| Çalışan               | Arama         | X            | X              |


**Çalışan Kişisel Ayrıntıları**

| Alanlar                             | Veri türü    | Gerekli | Aranabilir |
|------------------------------------|--------------|----------|------------|
| Doğduğu Şehir                         | Text         |          | X          |
| Doğduğu ülke/bölge            | Seçenek Kümesi   |          | X          |
| Doğum tarihi                          | Yalnızca Tarih    |          | X          |
| Vatandaşı olunan ülke/bölge      | Seçenek Kümesi   |          | X          |
| Ölüm tarihi                      | Yalnızca Tarih    |          | X          |
| Devre dışı gazilik doğrulama tarihi | Yalnızca Tarih    |          | X          |
| Eğitim                          | Text         |          | X          |
| Etnik Kökeni                     | Arama       |          | X          |
| ExpatriateEndDate                  | Yalnızca Tarih    |          | X          |
| ExpatriateStartDate                | Yalnızca Tarih    |          | X          |
| Baba Doğum Ülke veya Bölge     | Seçenek Kümesi   |          | X          |
| Cinsiyet                             | Seçenek Kümesi   |          | X          |
| Devre dışı bırakıldı                        | İki seçenek  |          | X          |
| Engelli Gazi                | İki seçenek  |          | X          |
| Sınır dışı etme kuralı geçerli mi?    | İki seçenek  |          | X          |
| Tam Zamanlı Öğrenci               | İki seçenek  |          | X          |
| Medeni Durum                     | Seçenek Kümesi   |          | X          |
| Askerlik hizmeti bitiş tarihi          | Yalnızca Tarih    |          | X          |
| Askerlik hizmeti başlangıç tarihi        | Yalnızca Tarih    |          | X          |
| Anne Doğum Ülke veya Bölge     | Seçenek Kümesi   |          | X          |
| Uyruk Ülke veya bölgesi      | Seçenek Kümesi   |          | X          |
| Ana dil                    | Arama       |          | X          |
| Bakmakla yükümlü olduğu kişi sayısı               | Tam sayı |          |            |
| Gazilik Durumu                     | Arama       |          | X          |
| Çalışan                             | Arama       | X        | X          |
| Çalışan personel ayrıntı numarası      | Text         | X        | X          |


**Çalışan banka hesabı**

| **Alanlar**                 | **Veri türü** | **Gerekli** | **Aranabilir** |
|----------------------------|---------------|--------------|----------------|
| Hesap sahibi             | Text          |              | X              |
| Hesap Tanımlayıcısı     | Text          |              | X              |
| Adres Açıklaması        | Text          |              | X              |
| Banka Hesabı Türü          | Seçenek Kümesi    |              | X              |
| Banka Konumu Kodu         | Text          |              | X              |
| Şube Adı                | Text          |              | X              |
| Şube Numarası              | Text          |              | X              |
| Şehir                       | Text          |              | X              |
| Ülke veya Bölge          | Text          |              | X              |
| İlçe                     | Text          |              | X              |
| Tanım                | Text          |              | X              |
| Bölge Adı              | Text          |              | X              |
| E-posta                      | Text          |              | X              |
| Dahili                  | Text          |              | X              |
| Faks                        | Text          |              | X              |
| IBAN                       | Text          |              | X              |
| Satır 1                     | Text          |              | X              |
| Satır 2                     | Text          |              | X              |
| Satır 3                     | Text          |              | X              |
| Cep Telefonu               | Text          |              | X              |
| Kişinin Adı             | Text          |              | X              |
| Posta Kodu                | Text          |              | X              |
| Posta Kutusu            | Text          |              |                |
| Rota Numarası             | Text          |              | X              |
| Rota Numarası Türü        | Seçenek Kümesi    |              | X              |
| İl veya İdari Bölge          | Text          |              | X              |
| SWIFT Kodu                 | Text          |              | X              |
| Telefon                  | Text          |              | X              |
| Teleks Numarası               | Text          |              | X              |
| Web Sitesi URL'si                | Text          |              | X              |
| Çalışan                     | Arama        | X            | X              |
| Çalışan Banka hesap numarası | Text          |              | X              |
| Çalışan Banka hesap numarası | Text          | X            | X              |

**Çalışan ücreti sabit**

| Alanlar                                | Veri türü      | Gerekli | Aranabilir |
|---------------------------------------|----------------|----------|------------|
| Şirket                               | Arama         | X        | X          |
| Maaş Türü                     | Seçenek Kümesi     |          | X          |
| Para Birimi                              | Arama         |          | X          |
| Yürürlük Tarihi                        | Yalnızca Tarih      |          | X          |
| Olay                                 | Arama         | X        | X          |
| Döviz Kuru                         | Ondalık sayısı |          | X          |
| Bitiş Tarihi                       | Yalnızca Tarih      |          | X          |
| Satır Numarası                           | Ondalık sayısı |          | X          |
| Ödeme Sıklığı                         | Arama         | X        | X          |
| Ödeme oOranı                              | Para Birimi       |          | X          |
| Ödeme Oranı (taban)                       | Para Birimi       |          | X          |
| Plan                                  | Arama         | X        | X          |
| Bölme                              | Arama         | X        | X          |
| İşlem Türü                          | Seçenek Kümesi     | X        | X          |
| Referans Noktası Ayarı Satırı            | Arama         |          | X          |
| Çalışan                                | Arama         | X        | X          |
| Çalışan sabit ücret numarası      | Text           | X        | X          |

**Çalışan Kişi Tanımlama Numarası**

| Alanlar                 | Veri türü   | Gerekli | Aranabilir |
|------------------------|-------------|----------|------------|
| Tanım            | Text        |          | X          |
| Giriş türü             | Text        |          | X          |
| Bitiş Tarihi        | Yalnızca Tarih   |          | X          |
| Kimlik Numarası  | Text        | X        | X          |
| Tanımlama türü    | Arama      | X        | X          |
| Birincil             | İki seçenek |          | X          |
| Düzenleme tarihi             | Yalnızca Tarih   |          | X          |
| Veren kurum         | Arama      | X        | X          |
| Çalışan                 | Arama      | X        | X          |


## <a name="position-entities"></a>Varlıkları Konumlandır

**İş Pozisyonu**

| **Alanlar**               | **Veri türü**  | **Gerekli** | **Aranabilir** |
|--------------------------|----------------|--------------|----------------|
| Etkinleştirme               | Tarih ve Saat  |              | X              |
| Atama için kullanılabilir | Tarih ve Saat  |              | X              |
| Departman               | Arama         |              | X              |
| Tanım              | Text           |              | X              |
| Tam zamanlı eş değeri     | Ondalık sayısı |              | X              |
| Görev                      | Arama         | X            | X              |
| İş Pozisyon Numarası      | Text           | X            | X              |
| Ana İş pozisyonu      | Arama         |              | X              |
| Pozisyon türü            | Arama         |              | X              |
| Emeklilik               | Tarih ve Saat  |              | X              |
| Ünvan                    | Seçenek Kümesi     |              | X              |
| Geçerlilik Başlangıcı               | Tarih ve Saat  | X            | X              |
| Geçerlilik Bitişi                 | Tarih ve Saat  |              | X              |


**Pozisyon türü**

| **Alanlar**         | **Veri türü** | **Gerekli** | **Aranabilir** |
|--------------------|---------------|--------------|----------------|
| Sınıflandırma     | Seçenek Kümesi    |              | X              |
| Tanım        | Text          |              | X              |
| Pozisyon türü adı | Text          | X            | X              |


**Pozisyon çalışan ataması**

| **Alanlar**                        | **Veri türü** | **Gerekli** | **Aranabilir** |
|-----------------------------------|---------------|--------------|----------------|
| İş Pozisyonu                      | Arama        | X            | X              |
| Çalışan pozisyon ataması numarası | Text          | X            | X              |
| Geçerlilik Başlangıcı                        | Text          | X            | X              |
| Geçerlilik Bitişi                          |               |              | X              |
| Çalışan                            |               | X            | X              |

## <a name="job-entities"></a>İş varlıkları

**İş**

| **Alanlar**                   | **Veri türü**  | **Gerekli** | **Aranabilir** |
|------------------------------|----------------|--------------|----------------|
| Sınırsız pozisyona izin ver    | İki seçenek    |              | X              |
| Varsayılan Tam zamanlı eşdeğeri | Ondalık sayısı |              | X              |
| Tanım                  | Text           |              | X              |
| İş Açıklaması              | Text           |              | X              |
| İş İşlevi                 | Arama         |              | X              |
| İş Türü                     | Arama         |              | X              |
| Maksimum pozisyon sayısı  | Tam sayı   |              | X              |
| Dosya Adı                         | Text           | X            | X              |
| Ünvan                        | Seçenek Kümesi     |              | X              |
| Geçerlilik Başlangıcı                   | Tarih ve Saat  | X            | X              |
| Geçerlilik Bitişi                     | Tarih ve Saat  |              | X              |


**İş işlevi**

| **Alanlar**        | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------------|---------------|--------------|----------------|
| Tanım       | Text          | X            | X              |
| İş İşlev adı | Text          | X            | X              |


**İş türü**

| **Alanlar**    | **Veri türü** | **Gerekli** | **Aranabilir** |
|---------------|---------------|--------------|----------------|
| Tanım   | Text          | X            | X              |
| Muafiyet durumu | Seçenek Kümesi    | X            | X              |
| İş türü adı | Text          | X            | X              |

## <a name="leave-and-absence-entities"></a>İzin ve devamsızlık varlıkları

**Ayrılma kaydı**

| **Alanlar**            | **Veri türü** | **Gerekli** | **Aranabilir** |
|-----------------------|---------------|--------------|----------------|
| Tahakkuk tarihi esası    | Yalnızca Tarih     | X            | X              |
| Fiili başlangıç tarihi    | Yalnızca Tarih     | X            | X              |
| Özel Tarih           | Yalnızca Tarih     | X            | X              |
| Tahakkuk Askıda.  | İki seçenek   |              | X              |
| LeaveEnrollmentNumber | Text          | X            | X              |
| İzin Planı            | Arama        | X            | X              |
| Başlangıç Tarihi            | Yalnızca Tarih     | X            | X              |
| Katman Tabanı            | Seçenek Kümesi    | X            | X              |
| Çalışan                | Arama        | X            | X              |


**Ayrılma Banka hareketi**

| **Alanlar**                    | **Veri türü**  | **Gerekli** | **Aranabilir** |
|-------------------------------|----------------|--------------|----------------|
| Tutar                        | Ondalık sayısı | X            | X              |
| Şirket                       | Arama         | X            | X              |
| Bankası hesap numarası bırak | Text           | X            | X              |
| İzin Planı                    | Arama         |              | X              |
| İzin Türü                    | Arama         | X            | X              |
| Hareket Tarihi              | Yalnızca Tarih      | X            | X              |
| Hareket Numarası            | Ondalık sayısı | X            | X              |
| Hareket türü              | Seçenek Kümesi     | X            | X              |
| Çalışan                        | Arama         | X            | X              |


**İzin planı**

| **Alanlar**        | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------------|---------------|--------------|----------------|
| Tahakkuk Sıklığı | Seçenek Kümesi    | X            | X              |
| Şirket           | Arama        | X            | X              |
| Tanım       | Text          |              | X              |
| İzin Türü        | Arama        | X            | X              |
| Dosya Adı              | Text          | X            | X              |
| Başlangıç Tarihi        | Yalnızca Tarih     | X            | X              |


**İzin İsteği**

| **Alanlar**           | **Veri türü** | **Gerekli** | **Aranabilir** |
|----------------------|---------------|--------------|----------------|
| Açıklama              | Text          | X            | X              |
| Şirket              | Arama        | X            | X              |
| İstek numarası bırak | Text          |              | X              |
| Talep tarihi         | Tarih ve Saat | X            | X              |
| Durum               | Seçenek Kümesi    | X            | X              |
| Çalışan               | Arama        | X            | X              |


**Ayrılma talebi ayrıntıları**

| **Alanlar**                  | **Veri türü**  | **Gerekli** | **Aranabilir** |
|-----------------------------|----------------|--------------|----------------|
| Tutar                      | Ondalık sayısı | X            | X              |
| İzin Tarihi                  | Tarih ve Saat  | X            | X              |
| İzin İsteği               | Arama         | X            | X              |
| Ayrılma talebi ayrıntıları numarası | Text           | X            | X              |
| İzin Türü                  | Arama         | X            | X              |


**İzin türü**

| **Alanlar**      | **Veri türü** | **Gerekli** | **Aranabilir** |
|-----------------|---------------|--------------|----------------|
| Şirket         | Arama        | X            | X              |
| Tanım     | Text          |              | X              |
| Kazanç Kodu    | Arama        |              | X              |
| İzin türü adı | Text          | X            | X              |


**İş takvimi**

| **Alanlar**  | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------|---------------|--------------|----------------|
| Şirket     | Arama        | X            | X              |
| Tanım | Text          |              | X              |
| Dosya Adı        | Text          | X            | X              |


**İş takvimi gün**

| **Alanlar**               | **Veri türü** | **Gerekli** | **Aranabilir** |
|--------------------------|---------------|--------------|----------------|
| Takvim Tarihi            | Yalnızca Tarih     | X            | X              |
| Şirket                  | Arama        |              | X              |
| Durum                   | Text          |              | X              |
| İş Takvimi            | Arama        | X            | X              |
| İş takvimi gün numarası | Text          | X            | X              |


**İş Takvimi Tatili**

| **Alanlar**  | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------|---------------|--------------|----------------|
| Dosya Adı        | Text          |              | X              |
| Tanım | Text          | X            | X              |


**Çalışma takvimi tatil satırı**

| **Alanlar**                        | **Veri türü** | **Gerekli** | **Aranabilir** |
|-----------------------------------|---------------|--------------|----------------|
| Tatil Tarihi                      | Yalnızca Tarih     | X            | X              |
| Dosya Adı                              | Text          |              | X              |
| İş Takvimi Tatili             | Arama        | X            | X              |
| Çalışma takvimi tatil satırı numarası | Text          | X            | X              |


**Çalışma Takvimi Zaman Aralığı**

| **Alanlar**                         | **Veri türü** | **Gerekli** | **Aranabilir** |
|------------------------------------|---------------|--------------|----------------|
| Şirket                            | Arama        |              | X              |
| Bitiş Saati                           | Tam sayı  |              | X              |
| Başlangıç Zamanı                         | Tam sayı  |              | X              |
| İş Takvimi                      | Arama        | X            | X              |
| İş Takvimi Gün                  | Arama        | X            | X              |
| Çalışma Takvimi Zaman Aralığı numarası | Text          | X            | X              |

## <a name="organization-entities"></a>Kuruluş varlıkları

**Şirket**

| **Alanlar**   | **Veri türü** | **Gerekli** | **Aranabilir** |
|--------------|---------------|--------------|----------------|
| Şirket kodu | Text          | X            | X              |
| Dosya Adı         | Text          | X            | X              |


**Departman**

| **Alanlar**        | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------------|---------------|--------------|----------------|
| Departman Numarası | Text          | X            | X              |
| Tanım       | Text          |              | X              |
| Dosya Adı              | Text          | X            | X              |
| Üst Departman | Arama        |              | X              |


**Para Birimi**

| **Alanlar**         | **Veri türü**  | **Gerekli** | **Aranabilir** |
|--------------------|----------------|--------------|----------------|
| Para Birimi Kodu      | Text           | X            | X              |
| Para Birimi Adı      | Text           | X            | X              |
| Para birimi kesinliği | Tam sayı   | X            | X              |
| Para birimi simgesi    | Text           | X            | X              |
| Varlık resmi       | Görüntü          |              |                |
| Döviz Kuru      | Ondalık sayısı | X            | X              |
| Organizasyon       | Arama         | X            | X              |
| Durum             | Seçenek Kümesi     |              | X              |

## <a name="payroll-entities"></a>Bordro varlıkları

**Ödeme döngüsü**

| **Alanlar**  | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------|---------------|--------------|----------------|
| Tanım | Text          | X            | X              |
| Sıklık   | Seçenek Kümesi    | X            | X              |
| Dosya Adı        | Text          | X            | X              |


**Ödeme dönemi**

| **Alanlar**           | **Veri türü** | **Gerekli** | **Aranabilir** |
|----------------------|---------------|--------------|----------------|
| Varsayılan Ödeme Tarihi | Yalnızca Tarih     |              | X              |
| Tanım          | Text          |              | X              |
| Ödeme Döngüsü            | Görünüm          | X            | X              |
| Ödeme Dönemi sayısı    | Text          | X            | X              |
| Dönem bitiş tarihi      | Yalnızca Tarih     | X            | X              |
| Dönem başlangıç tarihi    | Yalnızca Tarih     | X            | X              |
| Durum               | Seçenek Kümesi    |              | X              |


**Bordro kazanç kodu**

| **Alanlar**              | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------------------|---------------|--------------|----------------|
| Tanım             | Text          | X            | X              |
| Ödeme türüne dahil et | Seçenek Kümesi    | X            | X              |
| Üretken mi           | İki seçenek   | X            | X              |
| Dosya Adı                    | Text          |              | X              |
| Miktar birimi           | Seçenek Kümesi    |              | X              |
| FMLA saatleri izle        | İki seçenek   |              | X              |


**Vergi bölgesi**

| **Alanlar**        | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------------|---------------|--------------|----------------|
| Şehir              | Text          |              | X              |
| Ülke veya Bölge | Text          |              | X              |
| İlçe            | Text          |              | X              |
| Dosya Adı              | Text          | X            | X              |
| İl veya İdari Bölge | Text          |              | X              |


**Kazanç Hesaplama sıklığı ödeme dönemi**

| **Alanlar**                                      | **Veri türü** | **Gerekli** | **Aranabilir** |
|-------------------------------------------------|---------------|--------------|----------------|
| Kazanç Hesaplama Sıklığı                   | Arama        | X            | X              |
| Kazanç Hesaplama sıklığı ödeme dönemi sayısı | Text          | X            | X              |
| Ödeme Dönemi                                      | Arama        | X            | X              |


**Banka hesabı ödemeleri**

| **Alanlar**                       | **Veri türü**  | **Gerekli** | **Aranabilir** |
|----------------------------------|----------------|--------------|----------------|
| Tutar                           | Para Birimi       |              | X              |
| Tutar (Temel)                    | Para Birimi       |              | X              |
| Banka Hesabı                     | Arama         | X            | X              |
| Banka hesabı ödemeleri sayısı | Text           | X            | X              |
| Şirket                          | Arama         | X            | X              |
| Para Birimi                         | Arama         |              | X              |
| Döviz Kuru                    | Ondalık sayısı |              | X              |
| Kalanı mı                     | İki seçenek    |              | X              |
| Öncelik                         | Tam sayı   |              | X              |

**Kişi kimliği veren acentesi**

| **Alanlar**           | **Veri türü** | **Gerekli** | **Aranabilir** |
|----------------------|---------------|--------------|----------------|
| Adres Açıklaması  | Text          |              | X              |
| Adres Satırı 1       | Text          |              | X              |
| Adres Satırı 2       | Text          |              | X              |
| Adres Satırı 3       | Text          |              | X              |
| Şehir                 | Text          |              | X              |
| Ülke veya Bölge    | Seçenek Kümesi    |              | X              |
| İlçe               | Text          |              | X              |
| Tanım          | Text          |              | X              |
| E-posta                | Text          |              | X              |
| Dahili            | Text          |              | X              |
| Faks                  | Text          |              | X              |
| Veren kurum adı  | Text          | X            | X              |
| Cep Telefonu         | Text          |              | X              |
| Sayfa                 | Text          |              | X              |
| Posta Kodu          | Text          |              | X              |
| Posta Kutusu      | Text          |              | X              |
| Kısa mesaj                  | Text          |              | X              |
| İl veya İdari Bölge    | Text          |              | X              |
| Telefon            | Text          |              | X              |
| Teleks                | Text          |              | X              |
| Web Sitesi URL'si          | Text          |              | X              |

**Çalışan Kişi Tanımlama Türü**

| **Alanlar**                        | **Veri türü**  | **Gerekli** | **Aranabilir** |
|-----------------------------------|----------------|--------------|----------------|
| İzin verilen değer                    | Seçenek Kümesi     |              | X              |
| Ülke veya Bölge                 | Text           |              | X              |
| Tanım                       | Text           |              | X              |
| Sabit Uzunluk                      | Tam sayı   |              | X              |
| Kimlik saptama sayısı biçimi      | Text           |              | X              |
| Türü                              | Seçenek Kümesi     |              | X              |
| Çalışan Kişi Tanımlama Türü | Text           | X            | X              |

## <a name="fixed-compensation-entities"></a>Sabit Ücret varlıkları

**Maaş sabit planı**

| **Alanlar**                  | **Veri türü** | **Gerekli** | **Aranabilir** |
|-----------------------------|---------------|--------------|----------------|
| Şirket                     | Arama        | X            | X              |
| Ücret Izgarası           | Arama        |              | X              |
| Para Birimi                    | Arama        | X            | X              |
| Tanım                 | Text          | X            | X              |
| Yürürlük Tarihi              | Yalnızca Tarih     | X            | X              |
| Bitiş Tarihi             | Yalnızca Tarih     | X            | X              |
| İş Alım Kuralı                   | Seçenek Kümesi    | X            | X              |
| Dosya Adı                        | Text          | X            | X              |
| Aralık Dışında Toleransı      | Seçenek Kümesi    | X            | X              |
| Ödeme Sıklığı               | Arama        | X            | X              |
| İzin verilen önerisi      | İki seçenek   | X            | X              |
| Referans nokta satır ayarı  | Arama        |              | X              |
| Türü                        | Seçenek Kümesi    | X            | X              |

**Ücret kılavuzu**

| **Alanlar**                  | **Veri türü** | **Gerekli** | **Aranabilir** |
|-----------------------------|---------------|--------------|----------------|
| Şirket                     | Arama        | X            | X              |
| Para Birimi                    | Arama        |              | X              |
| Tanım                 | Text          | X            | X              |
| Yürürlük Tarihi              | Yalnızca Tarih     |              | X              |
| Bitiş Tarihi             | Yalnızca Tarih     |              | X              |
| Dosya Adı                        | Text          | X            | X              |
| Referans Noktası Ayarı       | Arama        | X            | X              |
| Türü                        | Seçenek Kümesi    | X            | X              |

**Tazminat düzeyi**

| **Alanlar**      | **Veri türü** | **Gerekli** | **Aranabilir** |
|-----------------|---------------|--------------|----------------|
| Tanım     | Text          |              | X              |
| Dosya Adı            | Text          | X            | X              |
| Türü            | Seçenek Kümesi     | X            | X              |

**Maaş ödeme sıklığı**

| **Alanlar**                  | **Veri türü**   | **Gerekli** | **Aranabilir** |
|-----------------------------|-----------------|--------------|----------------|
| Yıllık Dönüştürme Faktörü    | Ondalık sayısı  |              | X              |
| Şirket                     | Arama          | X            | X              |
| Tanım                 | Text            |              | X              |
| Saatlik dönüştürme faktörü    | Ondalık sayısı  |              | X              |
| Aylık dönüştürme faktörü   | Ondalık sayısı  |              | X              |
| Dosya Adı                        | Text            | X            | X              |
| Dönem                      | Seçenek Kümesi      |              | X              |
| Haftalık dönüştürme faktörü    | Seçenek Kümesi      |              | X              |


**Ücret referans noktası ayarı**

| **Alanlar**          | **Veri türü**   | **Gerekli** | **Aranabilir** |
|---------------------|-----------------|--------------|----------------|
| Şirket             | Arama          | X            | X              |
| Maaş Türü   | Seçenek Kümesi      | X            | X              |
| Tanım         | Text            | X            | X              |
| Dosya Adı                | Text            | X            | X              |

**Ücret referans noktalarını ayar çizgisi**

| **Alanlar**            | **Veri türü**   | **Gerekli** | **Aranabilir** |
|-----------------------|-----------------|--------------|----------------|
| Şirket               | Arama          | X            | X              |
| Tanım           | Text            | X            | X              |
| Satır Numarası           | Ondalık sayısı  | X            | X              |
| Dosya Adı                  | Text            | X            | X              |
| Referans Noktası Ayarı | Arama          | X            | X              |

**Ücret bölgesi**

| **Alanlar**      | **Veri türü** | **Gerekli** | **Aranabilir** |
|-----------------|---------------|--------------|----------------|
| Tanım     | Text          | X            | X              |
| Dosya Adı            | Text          | X            | X              |

**Maaş yapısı**

| **Alanlar**                    | **Veri türü**   | **Gerekli** | **Aranabilir** |
|-------------------------------|---------------  |--------------|----------------|
| Tutar                        | Para Birimi        |              | X              |
| Taban tutarı                   | Para Birimi        |              | X              |
| Şirket                       | Arama          | X            | X              |
| Maaş yapısı numarası | Text            | X            | X              |
| Para Birimi                      | Arama          |              | X              |
| Döviz Kuru                 | Ondalık sayısı  |              | X              |
| Kılavuz                          | Arama          | X            | X              |
| Raf                         | Arama          | X            | X              |
| Referans Noktası               | Arama          | X            | X              |
| Referans nokta satır ayarı    | Arama          | X            | X              |

**Sabit ücret etkinliği**

| **Alanlar**            | **Veri türü**   | **Gerekli** | **Aranabilir** |
|-----------------------|-----------------|--------------|----------------|
| Şirket               | Arama          | X            | X              |
| Tanım           | Text            | X            | X              |
| Olay Türü            | Seçenek Kümesi      | X            | X              |
| Etkin             | İki seçenek     | X            |                |
| Dosya Adı                  | Text            | X            | X              |

## <a name="entity-relationship-models"></a>Varlık ilişki modelleri

### <a name="worker"></a>Çalışan
![Çalışan](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>İş ve Iş pozisyonu
![İş ve Iş pozisyonu](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Kazançlar
![Kazançlar](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Ücret
![Ücret](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Bırak
![Bırak](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>İş Takvimi
![İş Takvimi](./media/HCMCommon-work-calendar-entity-diagram.png)
