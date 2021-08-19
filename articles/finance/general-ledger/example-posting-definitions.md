---
title: Deftere nakil tanımı örnekleri
description: Bu makale, deftere nakil tanımlarının satınalma siparişleri yükümlülükleri ve bütçe tahsis etme için nasıl kullanılacağına dair örnekler sağlar.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6dfd1012ccc1077a028c0cf082cd7685918579af6c58e498ddfa7f4dc9897c62
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764251"
---
# <a name="posting-definition-examples"></a>Deftere nakil tanım örnekleri

[!include [banner](../includes/banner.md)]

Bu makale, deftere nakil tanımlarının satınalma siparişleri yükümlülükleri ve bütçe tahsis etme için nasıl kullanılacağına dair örnekler sağlar.

Bu konuyu okumadan önce, nakil tanımlarını ve hareket nakil tanımlarını biliyor olmanız gerekir. Daha fazla bilgi için, bkz. [Nakil tanımları](posting-definitions.md). **Nakil tanımları** sayfasında aşağıdaki örnekler ayarlanabilir. Her bir örnek, şu bölümleri içerir:

-   Nakil tanımı – Eşleşme ölçütleri
-   Nakil tanımı – Üretilen girişler
-   Hesaplar, boyut değerleri ve tutarlar ile birlikte hareketler
-   Nakil tanımından üretilen genel muhasebe girişleri

Hareketteki nakil tanımı ve hesaplar ile boyut değerleri için **Eşleşme ölçütleri** bölmesinde hesaplar ile boyut değerleri arasında bir eşleşme ortaya çıktığında, genel muhasebe girişleri nakil tanımına yönelik **Üretilen girişler** bölmesi temel alınarak üretilir. 
> [!NOTE]
> Bir deftere nakil tanımını belirli bir hareket türü ile ilişkilendirmek için **İşlem deftere nakil tanımları** sayfasını kullanın. Bir deftere nakil tanımını bir hareket türü ile ilişkilendirdikten sonra, **Deftere nakil tanımları kullan** seçeneğini, **Genel muhasebe parametreleri** sayfasında seçin, seçilen hareket türünün tüm hareketleri, deftere nakil tanımlarını kullanmak zorundadır.

## <a name="example-purchase-order-encumbrances"></a>Örnek: Satınalma emri yükümlülükleri
**Genel muhasebe parametreleri** sayfasında **Yükümlülük işlemini etkinleştir** seçeneğini belirleyerek yükümlülük işlemesini etkinleştirdiğinizde, yükümlülükleri genel muhasebeye kaydetmek için rezerve edilmesi gereken tüm hesaplara yönelik nakil tanımlarının kullanılması gerekir. Çoğu durumda, tüm gider hesapları bilançoda rezerve edilir. 

Yükümlülüklere yönelik nakil tanımları, **Nakil tanımları** sayfasındaki, **Satınalma** modülünde ayarlanır. Ardından, **Hareket nakil tanımları** sayfasının **Satınalma** alanında **Satınalma emri** hareket türünü seçerek nakil tanımını satınalma emirleri ile ilişkilendirebilirsiniz. 

Satınalma emri yükümlülüğüne yönelik tüm fiş hareketleri, bir fiş üzerindeki her bir benzersiz boyutu dengelemelidir (yani borçlar kredilere eşit olmalıdır).

### <a name="posting-definition--match-criteria"></a>Nakil tanımı – Eşleşme ölçütleri

| Hesap yapısı       | Hesap numarasını eşleştir | Öncelik  |
|-------------------------|----------------------|----------|
| Hesap Yapısı - Kar ve Zarar | \*                   | 1        |

<em>**Hesap numarasını</em>* eşleştir alanında boş bir değer olması, tanımlı hesap yapısındaki tüm eşleşen hesapların eşleştirme kuralının parçası olduğu anlamına gelir.

### <a name="posting-definition--generated-entries"></a>Nakil tanımı – Üretilen girişler

| Hesap yapısı | Oluşturulan hesap numarası                    | Oluşturulan borç/alacak |
|-------------------|---------------------------------------------|------------------------|
| Kalan           | 300143 - -(Yükümlülük hesabı)             | Aynısı                   |
| Kalan           | 300144 - -(Yükümlülük hesabına rezerve et) | Dengeleme              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Hesaplar, boyut değerleri ve tutarlar ile birlikte hareketler

Hesaplar ve boyut değerleri ya bir satınalma emri satırı için girdiğiniz muhasebe dağılımlarından ya da satıcılar, maddeler, kategoriler ve boyut şablonları için varsayılan ayarlar temel alınarak otomatik olarak üretilen hesaplar ve boyutlardan gelir.

| Hesap + boyutlar           | Borç  | Alacak | Açıklama |
|--------------------------------|--------|--------|---------|
| 606400-OU\_1-OU\_3566-Eğitimi | 250.00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Nakil tanımından üretilen genel muhasebe girişleri

Yükümlülükleri kaydetmek için genel muhasebe girişleri üretilir.

| Hesap + boyutlar           | Borç  | Alacak | Açıklama |
|--------------------------------|--------|--------|---------|
| 300143-OU\_1-OU\_3566-Eğitimi | 250.00 |        |         |
| 300144-OU\_1-OU\_3566-Eğitimi |        | 250.00 |         |

Bu örnekte, Hesap Yapısı - Kar ve Zarar'ın parçası olan tüm hesaplar nakil tanımı kriterlerini karşılar. Dolayısıyla, 606500-OU\_1-OU\_3566-Eğitim değerlendirildiğinde, üretilen girişler, nakil tanımı için **Genel girişler** bölmesinde tanımlanan hesaplara yönelik oluşturulur.

## <a name="example-budget-appropriations"></a>Örnek: Bütçe tahsisatları
**Genel muhasebe parametreleri** sayfasındaki **Bütçe tahsisatını etkinleştir**'i seçerek bütçe tahsisatını etkinleştirdiğinizde, bütçe kayıt girişlerini genel muhasebeye kaydetmek için nakil tanımlarının kullanılması gereklidir. Bir bütçe kontrol yapılandırması aktif ve açık durumda iken, tahsisatlar, revizyonlar, transferler, projeler, sabit kıymetler ve genel muhasebeye tedarik ve talep tahminlerine yönelik girişlerin kaydını desteklemek için nakil tanımları ve hareket nakil tanımları kullanılabilir. 

**Orijinal bütçe** bütçe türüne sahip ve tahsisatları etkinleştirilmiş bütçe kaydı girişlerine yönelik bir nakil tanımı ayarlamak için, **Nakil tanımları** sayfasındaki **Bütçe** modülünü seçin. Ardından, **Hareket nakil tanımları** sayfasının **Bütçe** alanında, nakil tanımını bütçe türü **Orijinal bütçe** olan bütçe kaydı girişleri ile ilişkilendirmek için bütçe kodları kullanabilirsiniz. 

Bütçe tahsisatları ve nakil tanımları etkinleştirildiğinde, bütçe kaydı girişleri bütçe kontrolü için ve genel muhasebede kaydedilir.

### <a name="posting-definition--match-criteria"></a>Nakil tanımı – Eşleşme ölçütleri

| Hesap yapısı       | Hesap numarasını eşleştir | Öncelik  |
|-------------------------|----------------------|----------|
| Hesap Yapısı - Kar ve Zarar | \*                   | 1        |

<em>**Hesap numarasını</em>* eşleştir alanında boş bir değer olması, tanımlı hesap yapısındaki tüm eşleşen hesapların eşleştirme kuralının parçası olduğu anlamına gelir.

### <a name="posting-definition--generated-entries"></a>Nakil tanımı – Üretilen girişler

| Hesap yapısı | Oluşturulan hesap numarası              | Oluşturulan borç/alacak |
|-------------------|---------------------------------------|------------------------|
| Hesap yapısı | 300145 - -(Tahmini gelir hesabı) | Aynısı                   |
| Hesap yapısı | 300146 - -(Tahsisat hesabı)     | Dengeleme              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Hesaplar, boyut değerleri ve tutarlar ile birlikte hareketler

Bütçe hesabı girişine yönelik hesapları, boyut değerlerini ve tutarları **Bütçe kaydı girişi** sayfasına girersiniz.

| Hesap + boyutlar           | Borç | Alacak | Açıklama |
|--------------------------------|-------|--------|---------|
| 606400-OU\_1-OU\_3566-Eğitimi |       | 250.00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>Nakil tanımından üretilen genel muhasebe girişleri

Üretilen genel muhasebe girişleri, her bir boyutta orijinal bütçeyi kaydetmek için oluşturulur.

| Hesap + boyutlar           | Borç  | Alacak | Açıklama |
|--------------------------------|--------|--------|---------|
| 300145-OU\_1-OU\_3566-Eğitimi |        | 250.00 |         |
| 300146-OU\_1-OU\_3566-Eğitimi | 250.00 |        |         |

Bu örnekte, Hesap Yapısı - Kar ve Zarar'ın parçası olan tüm hesaplar nakil tanımı kriterlerini karşılar. Dolayısıyla 606400-OU\_1-OU\_3566-Eğitim değerlendirildiğinde, üretilen genel muhasebe girişleri oluşturulur.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]