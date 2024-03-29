---
title: Kıymet belgeleri
description: Bu makalede Kıymet Yönetimi'ndeki kıymet belgeleri açıklanmaktadır.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2e8d72dc938c43e266c6b7c39329f827c56607a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899483"
---
# <a name="asset-documents"></a>Kıymet belgeleri

[!include [banner](../../includes/banner.md)]

 

Bu makalede Kıymet Yönetimi'ndeki kıymet belgeleri açıklanmaktadır.

Kıymet Yönetimi'nde belgeleri örneğin iş türleriyle, kıymet üreticileriyle, kıymet türleriyle veya kıymetlerle otomatik olarak ilişkilendirilecek şekilde ayarlayabilirsiniz. Bu işlevsellik, güncelleştirilmiş belge sürümleri yayımlandığında yararlıdır. Bu durumda, güncelleştirilmiş belgeyi Supply Chain Management belgeleriniz için kullandığınız standart konuma koymanız ve bu belgeyi oluşturduğunuz varlık belgesi kaydına eklemeniz yeterlidir. Bundan sonra güncelleştirilmiş belgeye **Tüm kıymetler**, **Etkin kıymetler**, **Etkin kıymetlerim**, **Tüm iş emirleri** ve **Etkin iş emri işleri** menü öğelerinden erişebilirsiniz. Belgelerin bir varlık belgesi kaydına eklenmesi işleminde standart belge işleme sistemi kullanılır.

**Örnek 1:** Bir iş türüyle ilgili bir belge bu iş türü için bir yordamı tanımlayabilir.

**Örnek 2:** Bir kıymet türü, üretici ve model birleşimiyle ilgili bir belge seçili kıymet üreticisi modeli için standart kullanım kılavuzu olabilir.

## <a name="create-asset-document-relation"></a>Kıymet belgesi ilişkili oluşturma

1. **Kıymet yönetimi** \> **Kurulum** \> **Kıymet belgeleri**'ni seçin.
2. Bir kıymet belgesi kaydı oluşturmak için **Yeni**'yi seçin.
3. Tercih ettiğiniz belge ilişkisi ayrıntılarına bağlı olarak aşağıdaki alanların birinde veya birkaçında ilgili seçimleri yapın: **Kıymet türü**, **Üretici**, **Model**, **Kıymet**, **İş türü kategorisi**, **İş türü**, **İş türü çeşidi** ve **İş gereksinimi**. **İş türü çeşidi** ve **İş gereksinimi** alanlarındaki kullanılabilir seçenekler **İş türü** alanındaki seçiminize bağlıdır.

    > [!NOTE]
    > Sistem bir kıymet veya iş emriyle ilgili olması gereken belgeleri aradığında Kıymet Yönetimi olası eşleşmeleri denetlemek için tüm kıymet belgesi kayıtlarını tarar. Her zaman ilk önce en belirgin birleşimi denetler. Diğer bir deyişle, Kıymet Yönetimi önce **İş gereksinimi** alanı için bir eşleşme arar. Eşleşme bulamazsa **İş türü çeşidi** alanı için eşleşmeleri denetler. Eşleşme bulamazsa **İş türü** alanı için eşleşmeleri denetler ve bu şekilde devam eder. **Kıymet belgeleri** sayfasının düzeninde gördüğünüz gibi bu davranış en belirgin birleşimi bulmak için Kıymet Yönetimi'nin eşleşme için sağdan sola her kaydı denetleyeceği anlamına gelir. Bir kıymet veya iş emriyle birkaç belge ilgili olabilir. Bir bakım talebinin veya iş emrinin hizmet düzeyini gerektiği şekilde düzenleyebilirsiniz.

4. **Ekler**'i seçin. Standart **Belge işleme** sayfası görünür.
5. Kıymet belgesi kaydına eklenmesi gereken belgeleri veya notları ayarlayın. Belgeleri ekledikten sonra **Ekler** alanı kayıtla ilgili belgelerin sayısını gösterir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]