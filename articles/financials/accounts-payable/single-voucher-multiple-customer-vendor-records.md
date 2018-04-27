---
title: "Birden fazla müşteri veya satıcı kaydına sahip tek bir fiş"
description: "Bu konu, birden fazla müşteri veya satıcı kaydı içeren tek bir fişi deftere naklettiğinizde olacaklara ilişkin genel bir bakış sağlar. Bu işlevsellik, Microsoft Dynamics 365 for Finance and Operations'ın gelecekteki sürümlerinde durdurulacaktır. Sonuç olarak, kapatma işlemine muhasebe etkisi nedeniyle bu deftere nakletme yöntemini önermiyoruz."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4c499e31fb42a69dff6ac41faac0c78f7f4d1876
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Birden fazla müşteri veya satıcı kaydına sahip tek bir fiş

[!INCLUDE [banner](../includes/banner.md)]

Bu konu, birden fazla müşteri veya satıcı kaydı içeren tek bir fişi deftere naklettiğinizde olacaklara ilişkin genel bir bakış sağlar. Bu işlevsellik, Microsoft Dynamics 365 for Finance and Operations'ın gelecekteki sürümlerinde durdurulacaktır. Sonuç olarak, kapatma işlemine muhasebe etkisi nedeniyle bu deftere nakletme yöntemini önermiyoruz. 

Tek bir fişin birden fazla müşteri veya satıcı için kullanıldığı bazı yaygın örnekler, müşteriler arasındaki bakiye transferlerini ve aynı kuruluştaki müşteriler ve satıcılar arasındaki mahsuplaşma bakiyelerini içerir. 

Birden fazla müşteri veya satıcı içeren bir fiş aşağıdaki yöntemlerden biri kullanılarak girilebilir:

-   Günlüğe eklenen her satır aynı fişe dahil edilecek şekilde **Yalnızca bir fiş numarası** seçeneği belirlenmiş bir günlük kullanılarak.
-   Birden çok müşteri veya satıcı ile mahsup genel muhasebe hesabı olmayan birden çok satırlı bir fiş kullanılarak.
-   Hesapla ve satıcı/satıcı, müşteri/müşteri, satıcı/müşteri veya müşteri/satıcı olan mahsup hesabıyla bir fiş girerek.

Bu konu, birden fazla müşteri veya satıcı kaydı ile bir fiş deftere nakledildiğinde kapatmanın nasıl işleneceğini gösterir. Bu konu ayrıca, bir fişi birden fazla müşteri veya satıcıyla kullanmaktan nasıl kaçınacağınızı anlamanıza yardımcı olmak için geçici çözümler de sağlar. Özellikle bir fişin birden fazla müşteri veya satıcı ile kullanılmasından etkilenen iki genel kapatma senaryosunu gösteren örnekler bulunur.

-   Nakit iskontosu muhasebesi
-   Yeniden değerleme muhasebesi

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Kapatma tek bir fişin kullanımını nasıl etkiler
Birden çok müşteri veya satıcı kaydı içeren bir fiş nakledildiğinde birden çok alacak hesabı veya borç hesabı bakiyeleri içeren tek bir muhasebe fişi oluşturulur. Kapatma işlemi sırasında nakit iskontosu, gerçekleşmemiş kazanç ve zararlar, gerçekleşmiş kazanç ve zararlar ve orijinal belgenin özet hesabı yardımı için muhasebe girişleri oluşturmak üzere orijinal muhasebeleşme girişleri kullanılır. Örneğin, bir satıcı ödemesi bir fatura için kapatıldığında nakit iskontosu alınıyorsa nakit iskontosu muhasebesi, orijinal faturadan Borç hesapları genel muhasebe hesabına nakledilmelidir. Orijinal fatura birden çok satıcı kaydı içeren bir fişe nakledilirse orijinal muhasebeleşme özetlenir. Bu durumda, tek bir fişteki her bir satıcı hareketi için ayrıntılı muhasebe girişine erişmek mümkün olmadığından kullanıcının nakit iskontosunu nasıl muhasebeleştirmek istediği belirlenemez.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Birden çok satıcıya sahip bir fiş ve nakit iskontosu muhasebesi üzerinde etkisi

Aşağıdaki örnekte birden çok satıcı faturası **Genel günlük** sayfasındaki tek bir fiş üzerinden Genel muhasebeye kaydedilir. Bu faturalar birden çok hesap boyutu arasında dağıtılır.

|             |                  |              |                 |           |            |
|-------------|------------------|--------------|-----------------|-----------|------------|
| **Fiş** | **Hesap tipi** | **Hesap**  | **Açıklama** | **Borç** | **Alacak** |
| GNJL001     | Satıcı           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Satıcı           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Satıcı           | 1001         | INV3            |           | 300,00     |
| GNJL001     | Genel Muhasebe           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Genel Muhasebe           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Genel Muhasebe           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Genel Muhasebe           | 606300-004-- | INV3            | 300,00    |            |

Deftere nakilden sonra bir fiş oluşturulur.

|             |              |                  |                                    |
|-------------|--------------|------------------|------------------------------------|
| **Fiş** | **Hesap**  | **Deftere nakil türü** | **Hareket para birimi cinsinden tutar** |
| GNJL001     | 606300-001-- | Genel muhasebe günlüğü   | 50,00                              |
| GNJL001     | 606300-002-- | Genel muhasebe günlüğü   | 50,00                              |
| GNJL001     | 606300-003-- | Genel muhasebe günlüğü   | 200,00                             |
| GNJL001     | 606300-004-- | Genel muhasebe günlüğü   | 300,00                             |
| GNJL001     | 200110-001-  | Satıcı bakiyesi   | -100,00                            |
| GNJL001     | 200110-001-  | Satıcı bakiyesi   | -200,00                            |
| GNJL001     | 200110-001-  | Satıcı bakiyesi   | -300,00                            |

Fişin, tek bir fişte Satıcı bakiyesi türünü deftere nakletmek için üç giriş içerdiğine dikkat edin. 606300-001 için 50,00 borç ve 606300-002 için 50,00 borcun 200110-001 satıcı bakiyesi girişine mahsup edilmesinin amaçlandığını göstermenin bir yolu yoktur. Bunun nedeni, kullanıcının tek bir fişte birden çok satıcı kaydını girmiş olmasıdır.

Bu örneği kullanarak tek bir fiş kullanmanın akış kapatma muhasebesine etkisini analiz edebiliriz. 3,00 nakit iskontosu alarak 200,00 tutarında bir faturanın 197,00'sini ödediğinizi varsayalım. Nakit iskontosu değerinin fatura fişinin gider hesaplarından tüm boyutlara tahsis edildiğine dikkat edin. Bunun nedeni bir fişin, kullanıcının tek bir fişteki satıcı bakiyesini ilişkilendirmek için gider dağıtımlarını nasıl hedeflediğini göstermeden yukarıdaki faturaya nakledilmesidir.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Fiş** | **Hesap**  | **Deftere nakil türü**     | **Borç** | **Alacak** |
| APPAYM001   | 200110-001-  | Satıcı bakiyesi       | 197,00    |            |
| APPAYM001   | 110110-001-  | Banka                 |           | 197,00     |
| 14000056    | 520200-001-- | Satıcı nakit iskontosu |           | 0,25       |
| 14000056    | 520200-002-- | Satıcı nakit iskontosu |           | 0,25       |
| 14000056    | 520200-003-- | Satıcı nakit iskontosu |           | 1,00       |
| 14000056    | 520200-004-- | Satıcı nakit iskontosu |           | 1,50       |
| 14000056    | 200110-001-  | Satıcı bakiyesi       | 3,00      |            |

Kullanıcı orijinal faturadan tüm gider dağıtımları arasında tahsis edilen nakit iskontosundan memnun değilse faturaları kaydetmek için bir fiş yerine birden fazla fiş kullanılmalıdır. Bu örneğin başlangıcında, bir fiş yerine birden çok fişin Genel muhasebeye nasıl girildiği gösterilmiştir.

|             |                  |              |                 |           |            |                 |                    |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fiş** | **Hesap tipi** | **Hesap**  | **Açıklama** | **Borç** | **Alacak** | **Mahsup türü** | **Mahsup hesap** |
| GNJL001     | Satıcı           | 1001         | INV1            |           | 100,00     | Genel Muhasebe          | &lt;boş&gt;      |
| GNJL001     | Genel Muhasebe           | 606300-001-- | INV1            |   50,00   |            | Genel Muhasebe          | &lt;boş&gt;      |
| GNJL001     | Genel Muhasebe           | 606300-002-- | INV1            |   50,00   |            | Genel Muhasebe          | &lt;boş&gt;      |
| GNJL002     | Satıcı           | 1001         | INV2            |           | 200,00     | Genel Muhasebe          | 606300-003--       |
| GNJL003     | Satıcı           | 1001         | INV3            |           | 300,00     | Genel Muhasebe          | 606300-004--       |

Şimdi, INV2 ödendiğinde aşağıdaki giriş yapılır. Nakit iskontosunun mali boyutlarının, ilişkili giderin mali boyutlarını izlediğine dikkat edin.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Fiş** | **Hesap**  | **Deftere nakil türü**     | **Borç** | **Alacak** |
| APPAYM001   | 200110-001-  | Satıcı bakiyesi       | 197,00    |            |
| APPAYM001   | 110110-001-  | Banka                 |           | 197,00     |
| 14000056    | 520200-003-- | Satıcı nakit iskontosu |           | 3,00       |
| 14000056    | 200110-001-  | Satıcı bakiyesi       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Birden çok satıcıya sahip bir fiş ve gerçekleşmiş kazanç/zarar muhasebesi üzerinde etkisi

|             |                  |             |                 |           |            |                  |              |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| **Fiş** | **Hesap tipi** | **Hesap** | **Açıklama** | **Borç** | **Alacak** | **Hesap tipi** | **Hesap**  |
| GNJL001     | Satıcı           | 1001        | INV1            |           | 100,00     | Genel Muhasebe           | 606300-001-- |
| GNJL001     | Satıcı           | 1001        | INV2            |           | 200,00     | Genel Muhasebe           | 606300-002-- |

Aşağıdaki örnekte birden çok satıcı faturası **Genel günlük** sayfasındaki tek bir fiş üzerinden Genel muhasebeye kaydedilir. Bu faturalar birden çok hesap boyutu arasında dağıtılır. Deftere nakilden sonra bir fiş oluşturulur.

|             |              |                  |                                          |                                         |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| **Fiş** | **Hesap**  | **Deftere nakil türü** | **Hareket para birimi cinsinden tutar (Euro)** | **Muhasebe para birimi cinsinden tutar (ABD Doları)** |
| GNJL001     | 606300-001-- | Genel muhasebe günlüğü   | 100,00                                   | 114,00                                  |
| GNJL001     | 606300-002-- | Genel muhasebe günlüğü   | 200,00                                   | 228,00                                  |
| GNJL001     | 200110-001-  | Satıcı bakiyesi   | -100,00                                  | -114,00                                 |
| GNJL001     | 200110-001-  | Satıcı bakiyesi   | -200,00                                  | -228,00                                 |

Fişin, tek bir fişte Satıcı bakiyesi türünü deftere nakletmek için iki giriş içerdiğine dikkat edin. 606300-001 için borcun 100,00'den 200110-001'e satıcı bakiyesi girişine mahsup edilmesinin amaçlandığını göstermenin bir yolu yoktur. Bunun nedeni kullanıcının, tek bir fişte birden çok satıcı kaydı girmesidir. 

Bu örneği kullanarak tek bir fiş kullanmanın akış kapatma muhasebesine etkisini analiz edebiliriz. Muhasebe para biriminizin ABD Doları olduğunu ve yukarıdaki hareketlerin Euro hareket para birimine nakledildiğini varsayın. 200,00 Euro faturanın tamamını ödediğinizi ancak faturanızı ve ödemeyi deftere naklettiğiniz tarihler arasında döviz kurundaki değişiklik nedeniyle gerçekleşmiş bir zararla karşılaştığınızı varsayın. Gerçekleşmiş zarar hesabı değerinin fatura fişinin gider hesaplarından tüm boyutlara tahsis edildiğine dikkat edin. Bu durumda, kullanıcının algısı yalnızca 002'nin kapatılan faturadaki gider hesabına ait olduğu şeklinde olsa da hem 001 hem de 002 boyutu tahsis edilir. Bunun nedeni bir fişin, kullanıcının tek bir fişteki satıcı bakiyesini ilişkilendirmek için gider dağıtımlarını nasıl hedeflediğini göstermenin bir yolu olmadan yukarıdaki faturaya nakledilmesidir.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Fiş** | **Hesap** | **Deftere nakil türü**   | **Hareket para birimi cinsinden tutar (Euro)** | **Muhasebe para birimi cinsinden tutar (ABD Doları)** |
| APPAYM001   | 200110-001- | Satıcı bakiyesi     | 200,00                                   | 230,00                                  |
| APPAYM001   | 110110-001- | Banka               | -200,00                                  | -230,00                                 |
| 14000056    | 801300-001- | Döviz kur farkı zararı | 0,00                                     | 0,67                                    |
| 14000056    | 801300-002- | Döviz kur farkı zararı | 0,00                                     | 1,33                                    |
| 14000056    | 200110-001- | Satıcı bakiyesi     |                                          | -2,00                                   |

Kullanıcı orijinal faturadan tüm gider dağıtımları arasında tahsis edilen Döviz kuru zararından memnun değilse faturaları kaydetmek için bir fiş yerine birden fazla fiş kullanılmalıdır. Bu örneğin başlangıcında, bir fiş yerine birden çok fişin Genel muhasebeye nasıl girildiği gösterilmiştir.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fiş** | **Hesap tipi** | **Hesap** | **Açıklama** | **Borç** | **Alacak** | **Mahsup türü** | **Mahsup hesap** |
| GNJL002     | Satıcı           | 1001        | INV1            |           | 100,00     | Genel Muhasebe          | 606300-001--       |
| GNJL003     | Satıcı           | 1001        | INV2            |           | 200,00     | Genel Muhasebe          | 606300-002--       |

Şimdi, INV2 ödendiğinde aşağıdaki giriş yapılır. Döviz kuru zararı mali boyutlarının, ilişkili giderin mali boyutlarını izlediğine dikkat edin.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Fiş** | **Hesap** | **Deftere nakil türü**   | **Hareket para birimi cinsinden tutar (Euro)** | **Muhasebe para birimi cinsinden tutar (ABD Doları)** |
| APPAYM001   | 200110-001- | Satıcı bakiyesi     | 200,00                                   | 230,00                                  |
| APPAYM001   | 110110-001- | Banka               | -200,00                                  | -230,00                                 |
| 14000056    | 801300-002- | Döviz kur farkı zararı | 0,00                                     | 2.00                                    |
| 14000056    | 200110-001- | Satıcı bakiyesi     |                                          | -2,00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Bakiye transferleri ve netleştirme senaryoları için bir fiş
Birden fazla müşteri veya satıcı içeren bir fişin kullanıldığı iki yaygın senaryo, bir müşteriden/satıcıdan başka bir müşteriye/satıcıya bakiye transferlerini ve aynı kuruluştaki bir müşterinin ve satıcının mahsuplaşmasını içerir. Aşağıdaki iki örnek, bu senaryoları bir fişe girmeye alternatif olarak bunları Dynamics 365 for Finance and Operations'a girmek için tercih edilen yöntemleri gösterir. 

*Bakiye transferi* birden çok müşteri içeren bir fiş olup bakiyenin bir müşteriden başka bir müşteriye (satıcılar için de aynı) transferi amacıyla girilir. Bir alt şirketin sorumluluğunun bir ana şirkete geçmesi gibi fatura ödeme sorumluluğu başka bir tarafa geçtiğinde bu senaryo gerçekleşir. 

Bu örnekte, ödeme 10 gün içinde yapıldığında müşterinin nakit iskontosu için uygun olduğu bir satış varsayılır. Bu örnekteki müşteri, faturayı ödemekten sorumlu bir sigorta şirketi kullanır. Sigorta şirketi, sistemde ikinci bir müşteri olarak ayarlanır. Orijinal müşterinin bakiyesi iskonto dönemi içinde %2 nakit iskontosu alarak faturayı ödeyen sigorta şirketine transfer edilir. 

Göstermek için, ACME müşterisine aşağıdaki satışın yapıldığını varsayalım. Aşağıdaki muhasebe girişleri satışı temsil eder.

|                    |                  |           |            |
|--------------------|------------------|-----------|------------|
| **Genel muhasebe hesabı** | **Deftere nakil türü** | **Borç** | **Alacak** |
| 401100-002-023-    | Gelir          |           | 100        |
| 130100-002-        | Müşteri bakiyesi | 100       |            |

Ardından, kullanıcı Alacak hesapları ödeme günlüğündeki bir fişte ACME'den sigorta şirketine borç bakiyesini transfer eder. Finance and Operations'da sigorta şirketi müşteri Sigortası olarak ayarlanır.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fiş** | **Hesap tipi** | **Hesap** | **Açıklama** | **Borç** | **Alacak** | **Mahsup türü** | **Mahsup hesap** |
| ARPAYM001   | Müşteri         | ACME        | Transfer et        |           | 100,00     | Müşteri        | Sigorta          |

Yukarıdaki girişin bir fişe dahil edildiğini dikkate alın. Bu fiş, iki müşteri kaydı içerir. Yukarıdaki Genel muhasebe girişi nakledildiğinde aşağıdaki fiş oluşturulur.

|             |             |                  |                                    |
|-------------|-------------|------------------|------------------------------------|
| **Fiş** | **Hesap** | **Deftere nakil türü** | **Hareket para birimi cinsinden tutar** |
| ARPAYM001   | 130100-002- | Müşteri bakiyesi | 100,00                             |
| ARPAYM001   | 130100-002- | Müşteri bakiyesi | -100,00                            |

Ardından Sigorta müşterisinden 98,00 için bir ödeme aldığınızı ve bakiye transferi ile oluşturulan faturayla ödemeyi kapatmayı seçtiğinizi varsayın. Bu, aşağıdaki fişin deftere nakledilmesiyle sonuçlanır. Kapatmanın orijinal faturadan mali boyutları kullanması beklentisi olabilir ancak Sigorta müşterisi için bir fatura belgesi olmadığından bu mümkün değildir. Varsayılan olarak nakit iskontosundaki dağıtım boyutlarının orijinal faturanın gelir hesabından değil transferden oluşturulan müşteri hareketinden geldiğine dikkat edin. Varsayılan, bakiyeleri transfer etmek için bir fişin kullanılmasının sonucudur.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Fiş** | **Hesap** | **Deftere nakil türü** | **Borç** | **Alacak** |
| ARPAYM002   | 110110-002- | Banka             | 98,00     |            |
| ARPAYM002   | 130100-002- | Müşteri bakiyesi |           | 98,00      |

Nakit iskontosuna ilişkin fişte mali boyut için varsayılan, transferden oluşturulan müşteri hareketinden gelir, çünkü transferde birden fazla müşteri vardır.

|             |             |                        |           |            |
|-------------|-------------|------------------------|-----------|------------|
| **Fiş** | **Hesap** | **Deftere nakil türü**       | **Borç** | **Alacak** |
| ARP-00001   | 403300-002- | Müşteri nakit iskontosu | 2.00      |            |
| ARP-00001   | 130100-002- | Müşteri bakiyesi       |           | 2.00       |

Kullanıcı bir fiş yerine nakit iskontosuna ilişkin mali boyutlar için varsayılandan memnun değilse bakiye transferini kaydetmek için birden fazla fiş kullanılmalıdır. Bu senaryo, bakiyenin TARAFINDAN TAŞINACAK olduğu müşteri için alacak faturası ve bakiyenin TAŞINACAĞI müşteri için oluşturulan bir alacak faturası veya fatura oluşturularak gerçekleştirilebilir. Aşağıdaki örnek, bu örneğin başında gösterildiği gibi, bakiyeyi transfer etmek için bir fiş kullanmak yerine birden çok fişin borç hesabı ödeme günlüğüne nasıl girildiğini gösterir.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fiş** | **Hesap tipi** | **Hesap** | **Açıklama** | **Borç** | **Alacak** | **Mahsup türü** | **Mahsup hesap** |
| ARPAYM001   | Müşteri         | ACME        |                 |           | 100,00     | Genel Muhasebe          | 401100-002-023-    |
| ARPAYM002   | Müşteri         | Sigorta   |                 | 100,00    |            | Genel Muhasebe          | 401100-002-023-    |

Bunun anlamı ARPAYM02 fişi ile Sigorta müşterisi 98,00 ödediğinde ARPAYM002 fişinin genel muhasebe hesap girişinden doğru mali boyutlar kullanılır.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Fiş** | **Hesap** | **Deftere nakil türü** | **Borç** | **Alacak** |
| ARPAYM003   | 110110-002- | Banka             | 98,00     |            |
| ARPAYM003   | 130100-002  | Müşteri bakiyesi |           | 98,00      |

Mali boyutlar, nakit iskontosu için ilgili fiş üzerinden ARPAYM002 fişinde gösterilen mahsuplaşma gelir hesabından kullanılır.

|             |                 |                        |           |            |
|-------------|-----------------|------------------------|-----------|------------|
| **Fiş** | **Hesap**     | **Deftere nakil türü**       | **Borç** | **Alacak** |
| ARP-00001   | 403300-002-023- | Müşteri nakit iskontosu | 2.00      |            |
| ARP-00001   | 130100-002-     | Müşteri bakiyesi       |           | 2.00       |

### 

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Birden çok müşteri ve satıcı için mahsuplaşmaya sahip bir fiş
Kuruluş, aynı şirket için satınalma ve satış gerçekleştirdiğinde mahsuplaşma yararlı olabilir. Müşteri faturaları için ödeme almayı beklemek ve satıcı faturalarına ödeme yapmak yerine satıcı ve müşteri faturaları netleştirilir. Mahsuplaşma hareketi devreden bakiyelere karşılık kapatılır. 

Göstermek için, satıcı 1001 ve müşteri US-008'in aynı müşteri olduğunu varsayalım. Bu durumda, kuruluşunuz kalan bakiyeyi ödemeden/almadan önce borç ve alacak bakiyelerini mahsuplaştırmak ister. Müşteri kaydının 75,00 Euro ve satıcı kaydının 100,00 Euro'ya sahip olduğunu varsayalım. Bunun anlamı bakiyeleri mahsuplaştırmayı tercih etmeniz ve satıcıya yalnızca 25,00 Euro ödeyecek olmanızdır. Ayrıca muhasebe para biriminin ABD Doları olduğunu varsayalım. Bu durumda, mahsuplaştırma hareketi alacak hesabı ödeme günlüğündeki bir fişe girilir.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fiş** | **Hesap tipi** | **Hesap** | **Açıklama** | **Borç** | **Alacak** | **Mahsup türü** | **Mahsup hesap** |
| APPAYM001   | Satıcı           | 1001        | Mahsuplaşma         |  75,00    |            | Müşteri        | US-008             |

Bu hareket için istenmeyen sorunlardan kaçınmak için bir fiş kullanmak yerine mahsuplaştırma hareketini kaydetmek üzere günlüğe birden çok fiş girilmelidir. Birden çok müşteri ve satıcı bakiyesi içeren bir fişi kullanmaktan kaçınmak için müşteri ve satıcı bakiyelerinin kliring hesabı ile mahsup edildiğine dikkat edin.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fiş** | **Hesap tipi** | **Hesap** | **Açıklama** | **Borç** | **Alacak** | **Mahsup türü** | **Mahsup hesap** |
| 001         | Müşteri         | US-008      |                 |           |  75,00     | Genel Muhasebe          | 999999---          |
| 002         | Satıcı           | 1001        |                 |  75,00    |            | Genel Muhasebe          | 999999---          |






