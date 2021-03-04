---
title: Uyumluluk oluşturma ve işleme
description: Uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmeyi bu konu açıklar.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439562"
---
# <a name="create-and-process-a-conformance"></a>Uyumluluk oluşturma ve işleme

[!include [banner](../../includes/banner.md)]

Uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmeyi bu konu açıklar. Bu kaydı USMF demo şirketinde çalıştırabilir ve önerilen değerleri kullanabilirsiniz. Tipik olarak, bu yordam kalite görevlisi tarafından gerçekleştirilir.  Önkoşul olarak, [Malların kalitesini incele](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) içindeki talimatlar bakın. Bir uygunsuzluk onayını işlemek için görev kaydını çalıştıran kullanıcının atanmış kullanıcılar sayfasında bir "Ad" değeri olmalıdır. Kullanıcının belge notları kullanabilmesi için belge işleme seçeneğinin kullanıcı ayarlarında etkinleştirilmiş olması gerekir.


## <a name="select-a-quality-order"></a>Bir kalite emri seçin
1. Gezinti panelinde **Modüller > Stok yönetimi > Periyodik görevler > Kalite yönetimi > Kalite emirleri** öğesine gidin.
2. Listede, [Malların kalitesini incele](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) içinde oluşturulmuş kalite emrini seçin.  

## <a name="create-a-nonconformance"></a>Uygunsuzluk oluşturma
1. Eylem Bölmesi'nde, **Sorgular**'ı seçin.
2. **Uyumsuzluklar**'ı seçin.
3. **Yeni**'yi seçin.
4. **Problem türü** alanının açılı menüsünde, denetleme işlemi sırasında bulunan problemi seçin.  
5. **Tamam**'ı seçin.

## <a name="approvereject-a-nonconformance"></a>Bir uygunsuzluğu onaylama/reddetme
1. **İşlevler**'i seçin.
2. **Uyumsuzluğu onayla**'yı seçin. Bu örnek için, uygunsuzluğu onaylayın. Onaylanan uygunsuzluklar, ilgili operasyonlar ile uygunsuzluk işleme sürecinin bir parçası olarak yerine getirilen işlerin kaydını tutmak ve, bu konuda olduğu gibi, uygunsuzluk işlemesini işlemden geçirmek için ilişkilendirilebilir.  
3. **Evet**'i seçin.

## <a name="create-a-correction-action"></a>Düzeltme eylemi oluşturma
1. **Düzeltmeler**'i seçin.
2. **Yeni**'yi seçin.
3. Yeni satırın **Personel numarası** alanında, açılır menüden istenilen kaydı seçin.
4. **Seç**'e tıklayın.
5. **Ekle**'yi seçin. Düzeltme hakkında bir not oluşturun. Bu örnek için eylem, uygunsuzluk durumunu tartışmak için satıcıya başvurmaktır.  
6. **Yeni**'yi seçin.
7. **Not**'u seçin. Rapor kurulumuna bağlı olarak, uygunsuzluk yönetimiyle ilgili raporların üzerine farklı belge türlerinin yazdırılabilir.  
8. **Tanım** alanına bir değer girin.
9. Sayfayı kapatın.

## <a name="maintain-a-correction"></a>Bir düzeltmeyi yönet
1. **Tamamladı işaretle**'yi seçin.
2. **Tamam**'ı seçin.
3. Sayfayı kapatın.

## <a name="close-a-nonconformance"></a>Bir uygunsuzluğu kapat
1. **İşlevler**'i seçin.
2. **Uyumsuzluğu kapat**'ı seçin.
3. **Evet**'i seçin.
4. Sayfaları kapatın.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]