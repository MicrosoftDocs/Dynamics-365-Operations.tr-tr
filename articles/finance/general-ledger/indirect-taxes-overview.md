---
title: Satış vergisine genel bakış
description: Bu konuda, satış vergisi sistemine bir genel bakış verilmektedir. Satış vergisi kurulumunun öğeleri ve birlikte nasıl çalıştıkları açıklanmaktadır.
author: ShylaThompson
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12e776a83e00c669984a278ab06b913743d6e544
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348950"
---
# <a name="sales-tax-overview"></a>Satış vergisine genel bakış

[!include [banner](../includes/banner.md)]

Bu konuda, satış vergisi sistemine bir genel bakış verilmektedir. Satış vergisi kurulumunun öğeleri ve birlikte nasıl çalıştıkları açıklanmaktadır.

## <a name="overview"></a>Özet

Satış vergisi çerçevesi, farklı türlerdeki dolaylı vergileri destekler, örneğin satış vergisi, katma değer vergisi (KDV), ürün ve hizmet vergisi, birim tabanlı ücretler ve stopaj vergisi gibi. Bu vergiler, satın alma ve satış hareketleri sırasında hesaplanır ve belgelenir. Düzenli olarak vergi dairelerine bildirilmeleri ve ödenmeleri gerekir. 

Aşağıdaki diyagram vergi varlıklarının kurulumunu ve nasıl ilişkilendirildiğini gösterir.

[![Vergi ayarı varlıklarına genel bakışı gösteren diyagram.](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Bir şirketin dikkate alması gereken tüm satış vergileri için, bir satış vergi kodu tanımlanması gerekir. Bir satış vergisi kodu, bu satış vergisi için vergi oranlarını ve hesaplama kurallarını saklar. 

Her satış vergisi kodu, bir satış vergisi kapanış dönemine bağlanmalıdır. Satış vergisi kapatma dönemleri, satış vergisinin vergi dairesine bildirilmesi ve ödenmesi gereken tarihi tanımlar. Her satış vergisi kapatma dönemi bir satış vergisi kurumuna atanmalıdır. Satış vergi dairesi, satış vergisinin bildirildiği ve ödendiği varlığı temsil eder. Ayrıca satış vergisi raporunun düzenini de tanımlar. Satış vergisi makamları satıcı hesaplarıyla ilgili olabilir. Daha fazla bilgi için bkz. [Vergi kapatma dönemlerini ayarlama](tasks/set-up-sales-tax-settlement-periods.md).

Her satış vergisi kodu, bir genel muhasebe defteri nakil grubuna da bağlanmalıdır. Genel muhasebeye nakil grubu, için satış vergisi kodları tutarların deftere nakledileceğini ana hesapları belirtir. 

İsteğe bağlı satış vergisi raporlama kodları da tanımlanabilir. Bunlar satış vergisi kodu için hesaplanan çeşitli tutar türleri için satış vergisi kodlarına atanabilir. **Koda göre satış vergisi ödemesi** raporu, belirli bir satış vergisi kapatma dönemi ve aralığı için satış vergisi raporlaması koduna göre toplamları gösterir. 

Satış vergisinin hesaplanması ve nakledilmesi gereken tüm hareketlerin bir satış vergisi grubu ve bir madde satış vergisi grubu olmalıdır. Satış vergisi grupları hareketin tarafı (örneğin müşteri veya satıcı) ile ilişkiliyken, madde satış vergisi grupları hareketin kaynağına (örneğin madde ya da tedarik kategorisi gibi) ilişkilidirler. Vergi grupları vergi kodlarının listesini içerir. Hem satış vergisi grubunda hem de madde satış vergisi grubunda bulunan vergi kodları, harekete uygulanacak vergi kodlarıdır. 

Aşağıdaki tablo, vergi kurulumu için varlıkları ve sıralamayı açıklar.

| Kurulum faaliyeti                                                  | Gerekli/İsteğe bağlı ve açıklama                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ana hesapları oluştur.                                           | Gerekli. Satış vergisi işlevini ayarlamadan önce, şirketin vergileri ödemek ve kaydetmek için kullandığı ana hesapların oluşturulması gerekir.                                                                                                                                                                             |
| Satış vergisi için Genel muhasebe deftere nakil grupları ayarlayın.                     | Gerekli. Genel muhasebe deftere nakil grupları, satış vergilerinin kaydedileceği ve ödeneceği ana hesapları tanımlar.   Daha fazla bilgi için bkz. [Satış vergisi için Genel muhasebe deftere nakil grupları ayarlama](tasks/set-up-ledger-posting-groups-sales-tax.md).                                                                                 |
| Vergi dairesi ayarlama.                                   | Gerekli. Satış vergisi daireleri, verginin bildirilmesi ve ödenmesi gereken varlıklardır.    Daha fazla bilgi için bkz. [Satış vergi daireleri ayarlama](tasks/set-up-sales-tax-authorities.md).                                                                                                                                          |
| Satış vergisi kapatma dönemlerini ayarla.                            | Gerekli. Satış vergisi kapatma dönemleri, satış vergisinin ne zaman ve ne sıklıkta bildirilmesi ve ödenmesi gerektiği hakkında bilgiler içerir. Bir satış vergi dairesiyle ilişkilidirler.                                                                                                                                                       |
| Satış vergisi raporlama kodlarını ayarla.                               | İsteğe bağlı. Satış vergisi raporlama kodları, satış vergisi kodlarına birden fazla satış vergisi kodu için tutarları bir satış vergisi raporlama kodu altında bildirebilmek için atanabilir. Daha fazla bilgi için bkz. [Satış vergisi raporlama kodları ayarlama.](tasks/set-up-sales-tax-reporting-codes.md).                                         |
| Satış vergisi kodlarını ayarla.                                         | Gerekli. Satış vergisi kodları, her satış vergisi için hesaplama kuralları ve vergi oranlarını içerir. Satış vergisi kodları, satış vergisi kapatma periyoduyla ve genel muhasebeye nakil grubuyla ilişkilidir. Daha fazla bilgi için bkz. [Satış vergisi kodları ayarlama.](tasks/set-up-sales-tax-codes.md).                                |
| Satış vergisi gruplarını ayarla.                                        | Gerekli. Satış vergisi grupları, bir hareketin tarafı (müşteri vey satıcı) için uygulanan satış kodlarının listesini içerir. Belirli bir hareket için, satış vergisi grubundaki ve madde satış vergisi grubundaki satış vergisi kodlarının kesişimi, o harekete uygulanacak satış vergisi kodlarını belirler.                  |
| Madde satış vergisi gruplarını ayarla.                                   | Gerekli. Madde satış vergisi grupları hareketin kaynağı için (ürün, hizmet vb.) geçerli olan satış kodlarının listesini içerir. Belirli bir hareket için, satış vergisi grubundaki ve madde satış vergisi grubundaki satış vergisi kodlarının kesişimi, o harekete uygulanacak satış vergisi kodlarını belirler. Daha fazla bilgi için bkz. [Satış vergisi grupları ve madde satış vergisi grupları ayarlama](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md). |
| Uygulama parametreleri sayfaları üzerindeki satış vergisi parametreleri ayarlayın. | Gerekli. Genel muhasebe, alacak hesapları ve borç hesapları gibi farklı alanların, dolaylı vergilerin doğru hesaplanabilmesi için parametreler ayarlaması gerekir. Bu parametrelerin çoğu varsayılan değerlere sahip olmakla birlikte, her şirketin gereksinimlerine uyacak şekilde değiştirilmelidir.                                          |

## <a name="sales-tax-on-transactions"></a>Hareketler üzerindeki satış vergisi
Her hareket (satış/satınalma belgesi satırları, günlükler vb.) üzerinde, satış vergisini hesaplamak için bir satış vergisi grubu ve madde satış vergisi grubu girmeniz gerekir. Ana veriler (örneğin, müşteri, satıcı, madde ve tedarik kategori) üzerinde varsayılan grupları belirtilmiştir, ancak gerekirse bir hareketin gruplarını el ile değiştirebilirsiniz. Her iki grup da satış vergisi kodlarının listesini içerir ve iki listedeki satış vergisi kodlarının kesişimi, hareket için geçerli satış vergisi kodlarının listesini belirler. 

Her harekette, hesaplanan satış vergisine **Satış vergisi hareketi** sayfasını açarak bakabilirsiniz . Belgenin tamamını veya bir belge satırı için satış vergisi arayabilirsiniz. Bazı belgeler için (örneğin, satıcı faturası ve genel günlükler), özgün belge sapmış tutarlar gösteriyorsa, hesaplanan satış vergisi ayarlayabilirsiniz.

## <a name="sales-tax-settlement-and-reporting"></a>Satış vergisi kapatması ve deftere nakli
Satış vergisi, vergi dairesine düzenlenen aralıklarla (aylık, üç aylık, vb.) bildirilmeli ve ödenmelidir. Vergi hesaplarını aralık için kapatabilir genel muhasebe nakil gruplarında belirtildiği gibi vergi kapatma hesabındaki bakiyeleri mahsup edebilirsiniz. Bu işleve **Satış vergisini kapatma ve deftere nakletme** sayfasında erişebilirsiniz. Satış vergisinin kapatılacağı satış vergisi kapatma dönemini belirtmeniz gerekir. 

Satış vergisi ödemesi yapıldıktan sonra, satış vergisi kapatma hesabındaki bakiye, banka hesabına karşı dengelenmelidir. Eğer satış vergisi kapatma döneminde belirtilen satış vergisi dairesi, satıcı hesabıyla ilişkiliyse, satış vergisi bakiyesi bir açık satıcı faturası olarak nakledilir ve düzenli ödeme teklifine sahil edilebilir.

## <a name="conditional-sales-tax"></a>Koşullu satış vergisi
Koşullu satış vergisi, bir faturada ödenen gerçek tutara orantılı olarak ödenen bir satış vergisidir. Buna karşılık, standart satış vergisi, faturalama sırasında hesaplanır. Koşullu satış vergisi, vergi dairesine ödemenin nakledildiğinde ödenmesi gerekir, fatura nakledildiğinde değil. Fatura deftere nakledildiğinde, hareket satış vergisi defter raporu üzerinde bildirilmelidir. Ancak, hareketin satış vergisi ödeme raporundan hariç tutulması gerekir. 

Koşullu satış vergisi onay kutusunu Genel muhasebe parametreleri formunda seçerseniz, siz faturayı ödeyene kadar hiçbir satış vergisi kesintiye uğratılamaz. Bu bazı ülke/bölgelerde bir yasal zorunluluktur.

> [!NOTE]
> Koşullu satış vergisi onay kutusunu seçerseniz, bu işlevi desteklemek için satış vergisi kodları ve satış vergisi grupları ayarlamalı ve ayrıca genel muhasebe defteri nakletme grupları oluşturmalısınız. |

###  <a name="example"></a>Örnek

Satış vergisini her ay kapatırsınız. 15 Haziran'da 10.000 artı satış vergisi tutarında bir müşteri faturası oluşturuyorsunuz.
-   Satış vergisi yüzde 2.500, ya da tutarının yüzde 25'idir.
-   Fatura ödemesinin vadesi 30 Haziran'dır.

Fatura Haziran'da deftere nakledildiğinde genellikle kapatır ve 2.500'ü vergi dairesine ödersiniz, ödemeyi müşteriden almamış olsanız bile. 

Ancak, bir koşullu satış vergisi kullanıyorsanız, ödemeyi müşteriden 30 Temmuz'da aldığınızda, vergi dairesi ile kapatırsınız.

### <a name="postdated-check"></a>İleri tarih atılmış çek

Ödeme yöntemi olarak ileri tarih atılmış çek kullanırsanız, ödeme oluşturulduğunda banka hesabı temizlenmez. Bazı ülkelerde, ödeme bankada silindiğinde KDV 'gerçekleşmiş' sorumluluk olur yani ileri tarih atılmış çek kapatılır. Bunu **Nakit ve banka yönetimi > Kurulum > Nakit ve banka yönetimi parametreleri > İleri tarih atılmış çekler**'de **İleri tarih atılmış çekler düzenlendiğinde koşullu vergi gerçekleştir**'i seçerek etkinleştirebilirsiniz.

Daha fazla bilgi için bkz. [Stopaj vergisi ayarlama.](tasks/set-up-withholding-tax.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]