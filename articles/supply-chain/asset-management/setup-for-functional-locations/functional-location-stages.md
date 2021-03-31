---
title: İşlem yapılacak yerleşim yaşam döngüsü durumları
description: Bu konuda Kıymet Yönetimi'nde işlem yapılacak yerleşim durumlarının ve yaşam döngüsü modellerinin nasıl ayarlanacağı açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ded5fb032676a261566254427abcb642924451d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228743"
---
# <a name="functional-location-lifecycle-states"></a>İşlem yapılacak yerleşim yaşam döngüsü durumları

[!include [banner](../../includes/banner.md)]

 

Bu konuda Kıymet Yönetimi'nde işlem yapılacak yerleşim yaşam döngüsü durumlarının ve yaşam döngüsü modellerinin nasıl ayarlanacağı açıklanmaktadır. İşlem yapılacak yerleşim yaşam döngüsü durumları, bir işlem yapılacak yerleşimin geçebileceği oluşturuldu, etkin ve bitti gibi durumları tanımlar. Yaşam döngüsü durumlarından bağımsız olarak tüm işlem yapılacak yerleşimleri **Tüm işlem yapılacak yerleşimler** listesi sayfasından görüntüleyebilirsiniz. İşlem yapılacak yerleşimin durumunu değiştirmek için **Tüm işlem yapılacak yerleşimler** listesi sayfasından yerleşimi ve **İşlem yapılacak yerleşim durumunu güncelleştir**'i seçin.

## <a name="set-up-functional-location-lifecycle-states"></a>İşlem yapılacak yerleşim yaşam döngüsü durumlarını ayarla

1. **Kıymet yönetimi** > **Kurulum** > **İşlem yapılacak yerleşimler** > **Yaşam döngüsü durumları**'nı seçin.
2. Yeni bir işlem yapılacak yerleşim durumu oluşturmak için **Yeni**'yi seçin.
3. Durum kimliğini **Yaşam döngüsü durumu** alanına, işlem yapılacak yerleşim durumunun adını da **Ad** alanına ekleyin. **Yaşam döngüsü modelleri** alanında işlem yapılacak yerleşim durumunu kullanan işlem yapılacak yerleşim yaşam döngüsü modellerinin sayısını görebilirsiniz.
4. İşlem yapılacak yerleşimin bu durumda etkin olması gerekiyorsa, **Genel** hızlı sekmesindeki **Etkin** geçiş düğmesinde "Evet" seçeneğini belirleyin.
5. İşlem yapılacak yerleşimle aynı ada sahip bir kıymeti otomatik olarak oluşturulabilmesi ve bunu bu durumdaki işlem yapılacak yerleşime yüklenebilmesi isteniyorsa **Kıymet oluştur** geçiş düğmesinde "Evet" seçeneğini belirleyin.  
>[!NOTE]
>Bu geçiş düğmesi **İşlem yapılacak yerleşim türleri** formunda **Genel** hızlı sekmesindeki **Kıymet türü** alanıyla ilgilidir (**Kıymet yönetimi** > **Kurulum** > **İşlem yapılacak yerleşimler** > **İşlem yapılacak yerleşim türleri**).
6. Bu durumda işlem yapılacak yerleşimin adının değiştirilebilmesi isteniyorsa **Yerleşimi yeniden adlandır** geçiş düğmesinde "Evet" seçeneğini belirleyin.
7. Bu durumda işlem yapılacak yerleşime yeni alt yerleşimler eklenebilmesi isteniyorsa **Yeni alt yerleşimler** geçiş düğmesinde "Evet" seçeneğini belirleyin.
8. Bu durumda işlem yapılacak yerleşime kıymet yüklenebilmesi isteniyorsa **Kıymetleri yükle** geçiş düğmesinde "Evet" seçeneğini belirleyin.
9. Bu durumda işlem yapılacak yerleşimin silinebilmesi isteniyorsa **İşlem yapılacak yerleşimi sil** geçiş düğmesinde "Evet" seçeneğini belirleyin.
10. İşlem yapılacak yerleşimde yüklü olan tüm kıymetler için kıymet yaşam döngüsü durumunun otomatik olarak güncelleştirilebilmesi isteniyorsa **Yaşam döngüsü durumu** alanından bir kıymet durumu seçin. Örnek: Bir işlem yapılacak yerleşimi kapatırsanız ve işlem yapılacak yerleşim yaşam döngüsü durumunu "Bitti" olarak ayarlarsanız işlem yapılacak yerleşimde yüklü kıymetlerin yaşam döngüsü durumunu otomatik olarak "Kullanılmıyor" seçeneğine değiştirmek isteyebilirsiniz.


>[!NOTE]
>İşlem yapılacak yerleşim yaşam döngüsü durumlar, yaşam döngüsü modelleri ve türler iş emri yaşam döngüsü durumları, iş emri yaşam döngüsü modelleri ve iş emri türleri ile aynı şekilde ilgilidir ve kullanılırlar. 

## <a name="set-up-functional-location-lifecycle-models"></a>İşlem yapılacak yerleşim yaşam döngüsü modellerini ayarla

İşlem yapılacak yerleşimleriniz için gereken yaşam döngüsü durumlarını oluşturduğunuzda bunları gruplara bölebilirsiniz. Bu, farklı işlem yapılacak yerleşim türleri için kullanılabilecek yaşam döngüsü modeli akışı oluşturmak için yapılır. En az bir standart işlem yapılacak yerleşim yaşam döngüsü modeli oluşturulmalıdır.

1. **Kıymet yönetimi** > **Kurulum** > **İşlem yapılacak yerleşimler** > **Yaşam döngüsü modelleri**'ni seçin.
2. Yeni bir yaşam döngüsü modeli oluşturmak için **Yeni**'yi seçin.
3. Yaşam döngüsü modeli kimliğini **Yaşam döngüsü modeli** alanına, yaşam döngüsü modelinin adını da **Ad** alanına ekleyin. **İşlem yapılacak yerleşim türleri** ve **Yaşam döngüsü durumları** alanlarında yaşam döngüsü modelini kullanan işlem yapılacak yerleşim türlerinin sayısını ve yaşam döngüsü modelinde seçili durumların sayısını görebilirsiniz.
4. **Yaşam döngüsü durumları** hızlı sekmesinde modele eklenmesi gereken durumları seçin. Bu işlem **Kalan yaşam döngüsü durumları** bölümünde bir duruma ve ardından ![ileri ok](media/02-setup-for-functional-locations.png) düğmesine tıklayarak yapılır.
5. Model için tüm kullanılabilir durumları seçmek isterseniz ![tüm kullanılabilir aşamaları seç](media/03-setup-for-functional-locations.png) düğmesine tıklayın. Tüm durumlar **Seçili yaşam döngüsü durumları** bölümüne aktarılır.
6. Seçili bir durumu modelden kaldırmak isterseniz **Seçili yaşam döngüsü durumları** bölümünden ve ardından ![geri ok](media/04-setup-for-functional-locations.png) düğmesini seçin.
7. Seçili durumu takip edebilecek yaşam döngüsü durumlarını tanımlamak için **Yaşam döngüsü durumu güncelleştirmeleri**'ni seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]