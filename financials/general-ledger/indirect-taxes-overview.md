---
title: "Satış vergisi genel bakış"
description: "Bu makalede, satış vergisi sistemine bir genel bakış verilmektedir. Satış vergisi kurulumunun öğeleri ve birlikte nasıl çalıştıkları açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 1adee145d705f239e0c663d310234286478fead0
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-overview"></a>Satış vergisi genel bakış

Bu makalede, satış vergisi sistemine bir genel bakış verilmektedir. Satış vergisi kurulumunun öğeleri ve birlikte nasıl çalıştıkları açıklanmaktadır.

<a name="overview"></a>Özet
--------

Satış vergisi çerçevesi, satış vergisi, katma değer vergisi (KDV), mal ve hizmet vergisi (GST), birim temelli ücretler ve stopaj vergisi gibi dolaylı vergiler birçok türde destekler. Bu vergileri hesaplanır ve satınalma ve satış işlemleri sırasında belgelenmiştir. Düzenli olarak, bunlar bildirilen ve gerekir vergi kurumlarına ödenen. 

Aşağıdaki diyagram vergi varlıklarının kurulumunu ve nasıl ilişkilendirildiğini gösterir.

[![TaxOverview](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Her bir şirket için dikkate almalı, için satış vergisi, satış vergisi kodunun tanımlanması gerekir. Bir satış vergisi kodu, bu satış vergisi için vergi oranlarını ve hesaplama kurallarını saklar. 

Her satış vergisi kodu, bir satış vergisi kapanış dönemine bağlanmalıdır. Satış vergisi kapatma dönemleri, satış vergisinin vergi dairesine bildirilmesi ve ödenmesi gereken tarihi tanımlar. Her satış vergisi kapatma dönemi bir satış vergisi kurumuna atanmalıdır. Satış vergi dairesi, satış vergisinin bildirildiği ve ödendiği varlığı temsil eder. Ayrıca satış vergisi raporunun düzenini de tanımlar. Satış vergisi makamları satıcı hesaplarıyla ilgili olabilir. 

Her satış vergisi kodu, bir genel muhasebe defteri nakil grubuna da bağlanmalıdır. Genel muhasebeye nakil grubu, için satış vergisi kodları tutarların deftere nakledileceğini ana hesapları belirtir. 

İsteğe bağlı satış vergisi raporlama kodları da tanımlanabilir. Bunlar satış vergisi kodu için hesaplanan çeşitli tutar türleri için satış vergisi kodlarına atanabilir. **Koda göre satış vergisi ödemesi** raporu, belirli bir satış vergisi kapatma dönemi ve aralığı için satış vergisi raporlaması koduna göre toplamları gösterir. 

Satış vergisinin hesaplanması ve nakledilmesi gereken tüm hareketlerin bir satış vergisi grubu ve bir madde satış vergisi grubu olmalıdır. Satış vergisi grupları hareketin tarafı (örneğin müşteri veya satıcı) ile ilişkiliyken, madde satış vergisi grupları hareketin kaynağına (örneğin madde ya da tedarik kategorisi gibi) ilişkilidirler. Vergi grupları vergi kodlarının listesini içerir. Hem satış vergisi grubunda hem de madde satış vergisi grubunda bulunan vergi kodları, harekete uygulanacak vergi kodlarıdır. 

Aşağıdaki tablo, vergi kurulumu için varlıkları ve sıralamayı açıklar.

| Kurulum faaliyeti                                                  | Gerekli/İsteğe bağlı ve açıklama                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ana hesapları oluştur.                                           | Gerekli. Satış vergisi işlevini ayarlamadan önce, şirketin vergileri ödemek ve kaydetmek için kullandığı ana hesapların oluşturulması gerekir.                                                                                                                                                                             |
| Satış vergisi için Genel muhasebe deftere nakil grupları ayarlayın.                     | Gerekli. Genel muhasebe deftere nakil grupları, satış vergilerinin kaydedileceği ve ödeneceği ana hesapları tanımlar.                                                                                                                                                                                                                            |
| Vergi dairesi ayarlama.                                   | Gerekli. Satış vergisi daireleri, verginin bildirilmesi ve ödenmesi gereken varlıklardır.                                                                                                                                                                                                                                   |
| Satış vergisi kapatma dönemlerini ayarla.                            | Gerekli. Satış vergisi kapatma dönemleri, satış vergisinin ne zaman ve ne sıklıkta bildirilmesi ve ödenmesi gerektiği hakkında bilgiler içerir. Bir satış vergi dairesiyle ilişkilidirler.                                                                                                                                                       |
| Satış vergisi raporlama kodlarını ayarla.                               | İsteğe bağlı. Satış vergisi raporlama kodları, satış vergisi kodlarına birden fazla satış vergisi kodu için tutarları bir satış vergisi raporlama kodu altında bildirebilmek için atanabilir.                                                                                                                                                                 |
| Satış vergisi kodlarını ayarla.                                         | Gerekli. Satış vergisi kodları, her satış vergisi için hesaplama kuralları ve vergi oranlarını içerir. Satış vergisi kodları, satış vergisi kapatma periyoduyla ve genel muhasebeye nakil grubuyla ilişkilidir.                                                                                                                                        |
| Satış vergisi gruplarını ayarla.                                        | Gerekli. Satış vergisi grupları, bir hareketin tarafı (müşteri vey satıcı) için uygulanan satış kodlarının listesini içerir. Belirli bir hareket için, satış vergisi grubundaki ve madde satış vergisi grubundaki satış vergisi kodlarının kesişimi, o harekete uygulanacak satış vergisi kodlarını belirler.                  |
| Madde satış vergisi gruplarını ayarla.                                   | Gerekli. Madde satış vergisi grupları hareketin kaynağı için (ürün, hizmet vb.) geçerli olan satış kodlarının listesini içerir. Belirli bir hareket için, satış vergisi grubundaki ve madde satış vergisi grubundaki satış vergisi kodlarının kesişimi, o harekete uygulanacak satış vergisi kodlarını belirler. |
| Uygulama parametreleri sayfaları üzerindeki satış vergisi parametreleri ayarlayın. | Gerekli. Genel muhasebe, alacak hesapları ve borç hesapları gibi farklı alanların, dolaylı vergilerin doğru hesaplanabilmesi için parametreler ayarlaması gerekir. Bu parametrelerin çoğu varsayılan değerlere sahip olmakla birlikte, her şirketin gereksinimlerine uyacak şekilde değiştirilmelidir.                                          |

## <a name="sales-tax-on-transactions"></a>Hareketler üzerindeki satış vergisi
Her hareket (satış/satınalma belgesi satırları, günlükler vb.) üzerinde, satış vergisini hesaplamak için bir satış vergisi grubu ve madde satış vergisi grubu girmeniz gerekir. Ana veriler (örneğin, müşteri, satıcı, madde ve tedarik kategori) üzerinde varsayılan grupları belirtilmiştir, ancak gerekirse bir hareketin gruplarını el ile değiştirebilirsiniz. Her iki grup da satış vergisi kodlarının listesini içerir ve iki listedeki satış vergisi kodlarının kesişimi, hareket için geçerli satış vergisi kodlarının listesini belirler. 

Her harekette, hesaplanan satış vergisine **Satış vergisi hareketi** sayfasını açarak bakabilirsiniz . Belgenin tamamını veya bir belge satırı için satış vergisi arayabilirsiniz. Bazı belgeler için (örneğin, satıcı faturası ve genel günlükler), özgün belge sapmış tutarlar gösteriyorsa, hesaplanan satış vergisi ayarlayabilirsiniz.

## <a name="sales-tax-settlement-and-reporting"></a>Satış vergisi kapatması ve deftere nakli
Satış vergisi, vergi dairesine düzenlenen aralıklarla (aylık, üç aylık, vb.) bildirilmeli ve ödenmelidir. Microsoft Dynamics 365 işlemleri için vergi hesaplarını kapatmak için aralığı ve mahsup genel muhasebe nakil gruplarının belirtildiği gibi vergi mahsup hesabına bakiyeleri sağlayan işlevselliği sağlar. Bu işleve erişmek **kapatmak ve satış vergisi deftere** sayfa. Satış vergisi kapatma periyodunun satış vergisi ödenmesi için belirtmeniz gerekir. 

Satış vergisi ödemesi yapıldıktan sonra, satış vergisi kapatma hesabındaki bakiye, banka hesabına karşı dengelenmelidir. Eğer satış vergisi kapatma döneminde belirtilen satış vergisi dairesi, satıcı hesabıyla ilişkiliyse, satış vergisi bakiyesi bir açık satıcı faturası olarak nakledilir ve düzenli ödeme teklifine sahil edilebilir.

## <a name="conditional-sales-tax"></a>Koşullu satış vergisi
Koşullu satış vergisi için ödenen gerçek fatura miktarına orantılı olarak ödenen bir satış vergisidir. Buna karşılık, Saat Faturalama sırasında standart satış vergisi hesaplanır. Koşullu satış vergisi ödemesi nakledildiğinde değil Fatura deftere nakledildiğinde satış vergi dairesine ödenmesi gereken. Faturayı deftere naklettiğinizde, hareketin satış vergisi defteri raporu üzerinde bildirilmelidir. Ancak, hareketin satış vergisi ödeme rapordan tutulması gerekir. 

Genel muhasebe parametreleri formunda koşullu satış vergisi onay kutusunu seçerseniz, satış vergisi Fatura ödenene kadar kesinti. Bu, bazı ülkelerde/bölgelerde yasal bir gereksinimdir.

> [!NOTE]
> Koşullu satış vergisi onay kutusunu seçtiğinizde, satış vergisi kodları ve satış vergisi gruplarını ayarlamak ve genel muhasebe deftere nakil grupları, işlevlerini desteklemek için oluşturabilir. |

###  <a name="example"></a>Örnek

Her ay satış vergilerini. 15 Haziran 10.000 artı vergi bir müşteri faturası oluşturun.
-   Satış vergisi, yüzde 25'i veya 2.500 değil.
-   Fatura ödeme 30 Temmuz'da olur.

Genellikle kapatmak ve Haziran ayında Fatura deftere nakledildiğinde müşteriden ödemeyi almamanız olsa da 2.500 vergi dairesine ödemek gerekirdi. 

Ancak, bir koşullu satış vergisi kullanıyorsanız, ödeme müşteriden 30 Temmuz'da aldığınızda, vergi dairesi ile kapatın.


