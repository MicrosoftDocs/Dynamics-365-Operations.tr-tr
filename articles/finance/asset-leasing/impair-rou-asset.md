---
title: Kullanım hakkı varlıklarının değerini düşürme
description: Bu makalede, değer düşüşünü kaydeden ve Muhasabe Standartları Kodlaması Konu 842 (ACS 842) işletme kiralamasının varlık amortisman planlamasını düzelten bir işlev açıklanmaktadır.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f953b3a351859c6becba10a129bbb17b49be6290
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894127"
---
# <a name="impair-right-of-use-assets"></a>Kullanım hakkı varlıklarının değerini düşürme

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kullanım hakkı (ROU) varlığının defter tutarı düşürülebilir değilse varlığın değerinin düşüp düşmediğini test etmeniz gerekebilir. Varlığın değerinin düştüğünü belirlerseniz Varlık kiralama değer düşüşünü kaydedebilir ve amortisman planlamasını buna göre düzeltebilir. Bu makalede, bir değer düşüşünü kaydeden ve Muhasabe Standartları Kodlaması Konu 842 (ACS 842) işletme kiralamasının amortisman planlamasını düzelten bir işlev açıklanmaktadır. Aynı yöntem, Uluslararası Mali Raporlama Standardı 16 (IFRS 16) kiralamaları için de geçerlidir.

Kiralamanın IFRS 16 kapsamında finansal kiralama veya ASC 842 kapsamında işletme kiralaması olarak sınıflandırılmasına bakılmaksızın, ROU varlığının kalan bakiyesi kalan dönem sayısı için sabit esasa göre amorti edilir.

## <a name="impair-an-rou-asset"></a>ROU varlığının değerini düşürme

1. Değeri düşen kiralamaya gidin ve **Defterler**'i seçin.
2. Eylem bölmesinde **Değer düşüşü**'nü seçin.
3. Gösterilen iletişim kutusundaki **Değer düşüşü tutarı** alanına varlık değer düşüşü tutarını girin. ROU varlığını azaltmak için, pozitif bir değer girmeniz gerekir.
4. **Hareket tarihi** alanına, değer düşüşü girişinin deftere nakledilmesi gereken tarihi girin.
5. **Kalan dönemler** alanına, amortisman uygulanacak kalan ay sayısını girin.
6. Önerilen kıymet bakiyesini ve mali girişi oluşturulmadan veya deftere nakledilmeden önce görüntülemek için **Önizleme** seçeneğini ayarlayın.
7. Kiralama defterini kapatmak için **Defteri kapat**'ı **Evet** olarak ayarlayın. **Kiralamayı yeniden aç** durumunu kullanarak bu eylemi geri alabilirsiniz. Kapalı kiralamalar için girişler deftere nakledilemez ve kapalı kiralamalar düzeltilemez. 
8. Değer düşüşü girişini oluşturmak veya deftere nakletmek için **Deftere naklet**'i seçin.

    > [!NOTE]
    > Değer düşüklüğü hareketi deftere nakledildikten sonra yeni bir kitap sürümü oluşturulur.

    > Kira, bir işletim kirası olarak sınıflandırılıyorsa, değer düşüşü ardından aylık amortisman, sabit amortisman kullanılarak hesaplanır.

9. Değeri düşürülen varlık amortisman planlamasını görüntülemek için ilgili kiralama defterinin varlık amortisman planını açın. Şimdi varlık, **Kalan dönemler** alanına girdiğiniz ay sayısı boyunca sabit esasa göre değer düşüşüne uğrayacaktır.
10. Değer düşüşü gider günlüğü girişini görmek için, değeri düşürülen kiralama defterinin Eylem Bölmesinde **Varlık kiralama günlüğü**'nü seçin. Sistem, değer düşüşü gideri defere nakil hesabını borçlandıran ve varlık kiralama deftere nakil hesabını alacaklandıran bir günlük girişi oluşturur. 
11. ROU varlığının yeni defter değerini görüntülemek için kiralama defterinin eylem bölmesinde **Varlık hareketleri**'ni seçin.

## <a name="example-of-rou-asset-impairment"></a>ROU varlığının değerini düşürme örneği

Bu örnekte kiralama, sahipliği aktarmayan veya kiracıya satın alma seçeneği sunmayan özelleştirilmemiş bir varlıktır.

### <a name="setup"></a>Ayar

Aşağıdaki tablolarda, bu örnekte kullanılan kiralama için **Genel** ve **Ödeme planı satırları** sekmelerinde ayarlanan değerler gösterilir.

**Genel sekmesi**

| Alan                      | Değer            |
|----------------------------|------------------|
| Kıymetin adil değeri    | 600,000          |
| Alternatif borçlanma oranı | %7               |
| Bileşim aralığı       | Yıllık         |
| Varlık faydalı ömrü (ay) | 600              |
| Yıllık ödeme türü               | Normal yıllık ödeme |
| Başlangıç tarihi          | 01.01.2019       |

**Ödeme planı satırları sekmesi**

| Alan             | Değer      |
|-------------------|------------|
| Başlangıç tarihi        | 01.01.2019   |
| Dönem aralığı   | Monthly    |
| Dönemler           | 120        |
| Bitiş tarihi          | 31.12.2028 |
| Ödeme sıklığı | Yıllık   |
| Ödeme tutarı    | 10,000     |

### <a name="steps"></a>Adımlar

1. Bu makalenin önceki bölümlerinde açıklandığı gibi kiralamayı oluşturduktan sonra, kiralama defterine gidin ve ödeme planını onaylayın. Ardından, ilk kabul günlüğü girişini deftere nakledin. İlk ROU varlığı ve kira yükümlülüğü 70.235,81 ABD doları olmalıdır. Bu örnekte kiralama, ASC 842 kapsamında bir işletme kirası olarak sınıflandırılmıştır.
2. Kira ödemeleri, faiz giderleri ve amortisman giderleri için üç yılın geçtiği simülasyonunu oluşturmak için toplu iş günlük işlemeyi üç kez çalıştırın.
3. Üç toplu işin hepsini çalıştırdıktan sonra, kiralama defterine geri dönün ve ROU varlığı ile kiralama yükümlülüğünün geçerli defter değerini görüntülemek için yükümlülük ve varlık hareketleri tablolarını açın. Üç yıldan sonra, yükümlülüğün değeri yaklaşık -53.893,00 ABD doları, varlığın değeri yaklaşık 53.893,00 ABD doları olmalıdır. 

    Üç yıldan sonra, işletme değer düşüşü testlerini gerçekleştirir ve ROU varlığının 35.000 ABD doları değer düşüşüne uğradığını belirler. Şimdi bu değer düşüşünü kaydetmelisiniz.
    
4. Kiralama defterine gidin ve sonra eylem bölmesinde **Değer düşüşü**'nü seçin.
5. **Değer düşüşü parametresi** sayfasında aşağıdaki ayrıntıları girin.

    | Alan                  | Değer    |
    |------------------------|----------|
    | Değer düşüşü tutarı      | 35,000   |
    | Hareket tarihi       | 01.01.2022 |
    | Kalan dönemler      | 84       |
    | Naklet                   | Evet      |
    | Deftere nakletmeden önce önizle | Hayır       |
    | Defteri kapat             | Hayır       |

6. Bir değer düşüşü gideri günlük girişi oluşturulmuş ve deftere nakledilmiştir. Bunu görüntülemek için kiralama defterinde varlığın kiralama günlüğüne gidin. Değer düşüşü tutarının, Değer düşüşü gideri deftere nakil hesabına borç olarak ve ROU varlığı deftere nakil hesabına alacak olarak kaydedildiğine dikkat edin.

7. Değer düşüşünün net etkisini görmek için, yükümlülük ve varlık hareketleri tablolarına gidin. Değer düşüşü giderinin ROU varlığını azaltmasına rağmen kiralama yükümlülüğü defter tutarını değiştirmediğine dikkat edin.

Değer düşüşünün dikkate almanız gereken başka bir etkisi daha bulunur. ROU varlık tutarı artık kiralama yükümlülüğünden çok daha düşük olduğundan, tutar daha önce olduğundan farklı bir şekilde amorti edilmelidir. Özellikle, varlık artık hareket tarihinden başlayarak kalan 84 kiralama ayı boyunca sabit esasa göre amorti edilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
