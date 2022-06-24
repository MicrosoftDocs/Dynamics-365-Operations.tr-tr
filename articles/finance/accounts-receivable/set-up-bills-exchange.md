---
title: Kambiyo senetlerini ayarlama
description: Bu makalede, kambiyo senetlerini ayarlama adımları açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: kfend
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 91821b10afe7cdbabd0a58b61219ce29d686c5c9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874739"
---
# <a name="set-up-bills-of-exchange"></a>Kambiyo senetlerini ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, kambiyo senetlerini ayarlama adımları açıklanmaktadır.

Kambiyo senedi bir müşteriden gelen ve belirtilen bir tutarı, genelde bir banka olan, başka bir tarafın şirkete ödemesi gerektiğini belirten yazılı veya elektronik bir sipariştir. Bir satış siparişi faturası veya serbest metin faturası için ödeme olarak kambiyo senedi kullandığınızda müşteri hesabını alacaklandırırsınız. Müşteri kambiyo senedini bankaya ödeyene kadar bu alacak tutarı kambiyo senedi tarafından teminat altına alınır. Genelde faturayı vade tarihinde kambiyo senediyle kapatırsınız. Bankanızdan kambiyo senedinin karşılığının ödendiğine ilişkin bir bildirim aldığınızda kambiyo senedini kapatabilirsiniz. Kambiyo senedini aşağıdaki zamanlardan birinde bankanız üzerinden düzenleyebilirsiniz:

-   Vade tarihinde. Bu yaklaşıma tahsilat için havale adı verilir.
-   Vade tarihinden önce, genelde müşteri için ayarlanan ödeme şartlarında belirtilen iskonto tarihinde. Hareketi deftere naklettiğiniz zaman iskonto tutarı bir gider hesabına nakledilir. Banka müşteriden ödeme alana kadar, kalan tutar sizde pasif olarak tutulur. Bu yaklaşıma iskonto için havale adı verilir.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Kambiyo senetleri için deftere nakil profilleri ayarlama

Kambiyo senetleri, protestolu kambiyo senetleri, tahsilat için havale ve iskonto için havale ile kullanabileceğiniz deftere nakil profilleri ayarlamak için **Müşteri deftere nakil profilleri** sayfasını kullanın. **Özet hesap** alanında, kambiyo senedi tutarlarının nakledileceği özet hesabı seçin. Kambiyo senedi hareket türüne bağlı olarak bu hesaba borç veya alacak yazılır:
-   Kambiyo senetlerinde, bu hesap bir kambiyo senedi nakledildiğinde borçlandırılır ve iskonto için havale veya tahsilat için havale nakledildiğinde alacaklandırılır.
-   Protestolu kambiyo senetlerinde, bu hesap protestolu bir kambiyo senedi nakledildiğinde borçlandırılır.
-   Tahsilat için havalelerde, bu hesap bir tahsilat için havale nakledildiğinde borçlandırılır.
-   İskonto için havalelerde, bu hesap bir iskonto için havale nakledildiğinde borçlandırılır.

**Kapatma hesabı** alanında, kambiyo senedi tutarlarının nakledileceği nakit hesabını seçin. Hesap, bir kambiyo senedi kapatıldığında borçlandırılır. **Satış vergisi ön ödemeleri** alanında, ön ödemeler için kambiyo senetleri kullanıldığında, satış vergisi tutarlarının nakledileceği özet hesabı seçin. **İskonto hesabı borçları** alanında, iskonto havaleleri için iskonto tutarının deftere nakledileceği hesabı seçin. Bu hesap, bir iskonto için havale deftere nakledildiğinde alacaklandırılır.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Kambiyo senetleri için Alacak hesapları parametrelerini ayarlama

**Alacak hesapları parametreleri** sayfasında, kambiyo senetleri için varsayılan deftere nakil profilleri **Genel muhasebe ve satış vergisi** sekmesinde girilir. Numara serileri **Numara serileri** sekmesinde tanımlanır.

## <a name="set-up-journal-names-for-bills-of-exchange"></a>Kambiyo senetleri için günlük adları ayarlama


**Günlük adları** sayfasında, kambiyo senetleri için kullanılmak üzere en az beş günlük adı oluşturun. Günlük türleri şunlardır:
-   **Müşteriye düzenlenen kambiyo senedi** – Düzenlenen kambiyo senetleri günlüğü için bir günlük adı oluşturun.
-   **Müşteri protestolu kambiyo senedi** – Protestolu kambiyo senedi günlüğü için bir günlük adı oluşturun.
-   **Müşteriye yeniden düzenlenen kambiyo senedi** – Yeniden düzenlenen kambiyo senetleri günlüğü için bir günlük adı oluşturun.
-   **Müşteri banka havalesi** – Havale günlüğü için bir günlük adı oluşturun.
-   **Müşteri tarafından ödenen kambiyo senedi** – Kambiyo senetleri kapatma günlüğü için bir günlük adı oluşturun.

Her bir kambiyo senedi günlüğü için günlük fişi sayfasında, kambiyo senedi hakkında bilgiyi **Kambiyo senedi** sekmesinde girin. Bir kambiyo senedi günlük satırları deftere nakledildikten sonra, bunları **Kambiyo senedi günlük sorgusu** sayfasında ve **Kambiyo senedi istatistikleri** sayfasında görebilirsiniz.

## <a name="set-up-methods-of-payment-for-bills-of-exchange"></a>Kambiyo senetleri için ödeme yöntemleri ayarlama

**Ödeme yöntemleri** sayfasında, kambiyo senetleri için en az bir ödeme yöntemi ayarlayın. Birden fazla bankayla iş yapıyorsanız, her bankanın kambiyo senedi için istediği havale biçimine karşılık gelen bir ödeme yöntemi ayarlayın.

## <a name="set-up-payment-fees-for-bills-of-exchange"></a>Kambiyo senetleri için ödeme masrafları ayarlama

Ödeme masrafı, müşterilerden ödeme tahsil etme işlemiyle ilişkili bir masraftır. Her ödeme masrafıyla birden fazla ödeme masrafı kurulum satırı ilişkilendirilebilir. Ödeme masrafları için varsayılan tutarların nasıl hesaplanacağını denetlemek için ayar satırlarını kullanabilirsiniz. Örneğin, ödeme yöntemleri, ödeme belirtimleri, para birimleri ve dönemler için kurulum satırları oluşturabilirsiniz. Gün aralıklarına dayanarak yüzde veya tutar için kurulum satırları da oluşturabilirsiniz. Örneğin, bir ödemenin vade gecikmesi zaman uzunluğuna bağlı bir vade farkı yüzdesi ayarlayabilirsiniz. Banka **Tahsilat** veya **İskonto** gibi farklı havale türleri için ayrı masraflar borçlandırıyorsa, her havale türü için ayrı bir ödeme masrafı satırı ayarlayın.

## <a name="set-up-remittance-fees-for-bank-remittance-files"></a>Banka havale dosyaları için havale ücretleri ayarlama

**Banka hesapları** sayfasında, oluşturulan her havale dosyası için bir banka tarafından borçlandırılan havale masrafları ayarlayabilirsiniz. Havale ücretleri havale onaylandığında ve gerçekleşen ücret tutarları bilindiğinde nakledilir. Havale masrafları, müşterilerden tahsil edilen ve günlük satırlarına iliştirilen ödeme masraflarından farklıdır.

## <a name="set-up-document-layouts-for-bills-of-exchange"></a>Kambiyo senetleri için belge düzenleri ayarlama

**Banka hesapları** sayfasında **Ayarla**'ya tıklayın ve basılı kambiyo senedi belgeleri oluşturacağınız her banka hesabı için gerekli belge düzenini belirtin.

## <a name="set-up-customers-for-bills-of-exchange"></a>Kambiyo senetleri için müşteri ayarlama

**Müşteriler** sayfasındaki **Ödeme varsayılanları** sekmesinde, bir kambiyo senedi kullanarak ödeme yapmayı kabul etmiş her müşteri için, kambiyo senetlerine yönelik varsayılan bir ödeme yöntemi ayarlayabilirsiniz.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
