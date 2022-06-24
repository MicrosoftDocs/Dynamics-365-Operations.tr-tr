---
title: Koşul değerlendirmesi
description: Bu makalede, Kıymet Yönetimi'nde bir kıymet üzerinde bir koşul değerlendirme şablonu ve kayıt oluşturma açıklanmaktadır.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa326a01bb63bd0b59c0df7a3c751a5242a3dd37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872108"
---
# <a name="condition-assessment"></a>Koşul değerlendirmesi

[!include [banner](../../includes/banner.md)]

 

Bu makalede, Kıymet Yönetimi'nde bir kıymet üzerinde bir koşul değerlendirme şablonu ve kayıt oluşturma açıklanmaktadır. Koşul değerlendirmesi düzenli aralıklarla gerçekleştirilir ve birincil amaç kıymetler üzerindeki koşul verilerini oluşturup korumaktır. Önleyici bakım açısından bakıldığında, mevcut durum ve kalan yaşam süresi gibi önemli bilgileri izlemek önemlidir. Ayrıca, düzenli aralıklarla koşul değerlendirmesi yaparsanız, fabrikanızdaki makinelerin koşullarını izleyip karşılaştırabilirsiniz.

Koşul değerlendirmesi, ekipmanınızda birçok koşulu ölçmek ve izlemek için kullanılabilir. Örnek: Makinelerinizdeki titreşimleri ölçebilirsiniz. Çeşitli ekipman türleri üzerinde Kıymet Yönetimi'nde titreşim ölçümlerini kaydettikten sonra, en son kayıtlı değerlendirmelerde arama yapabilir ve titreşim ölçümlerini görebilirsiniz.

Koşul değerlendirmesi kıymetler üzerinde oluşturulur. Koşul değerlendirme yordamını gerçekleştirmeden önce bir kıymet türü üzerinde bir koşul değerlendirme şablonu ayarlayın. Koşul değerlendirmesinde şablonları kullanmanın nedeni, benzer kıymetlerde koşul verilerinin değişmesini önlemektir. Kıymet Yönetimi'nde koşul değerlendirmesini ayarlama ve kullanma sırası şudur: Önce gerekli koşul değerlendirme şablonlarını ayarlayın. Ardından **Kıymet türleri** formunda şablonları kıymet türleriyle ilişkilendirin. Son olarak **Kıymet** formunda bir kıymet üzerinde koşul değerlendirmesi kayıtları oluşturabilirsiniz.

## <a name="create-a-condition-assessment-template"></a>Koşul değerlendirme şablonu oluşturma

1. **Kıymet yönetimi** > **Kurulum** > **Kıymet türleri** > **Koşul değerlendirmesi** öğesini seçin.
2. Yeni bir şablon oluşturmak için **Yeni**'yi seçin.
3. **Şablon** alanına şablonu ekleyip kimliğini belirtin.
4. **Ad** alanında şablon için bir ad girin.
5. **Koşul değerlendirme satırları** hızlı sekmesinden uygun koşul türü ve ölçü birimi seçimi dahil olmak üzere koşul değerlendirmesi için gerekli satırları ekleyin.
6. **Kıymet türleri** hızlı sekmesinden koşul değerlendirme şablonunu kullanması gereken kıymet türlerini ekleyin.
7. Ekranın üst kısmındaki **Ayrıntılar** grubunda **Satırlar** ve **Kıymet türleri** alanlarında seçili koşul değerlendirme şablonuyla ilgili değerlendirme satırlarının ve kıymet türlerinin sayısını görürsünüz.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Kıymette koşul değerlendirme kaydı oluşturma

1. **Kıymet yönetimi** > **Ortak** > **Kıymetler** > **Tüm Kıymetler** öğesini seçin.
2. Listede bir koşul değerlendirme kaydı oluşturmak istediğiniz kıymeti seçin.
3. **Genel** sekmesinde, **Koşul değerlendirmesi** seçeneğine tıklayın.
4. Yeni kayıt yapmak için **Yeni**'yi seçin.
5. **Tarih** alanında koşul değerlendirmesinin tarihini seçin.
6. **Çalışan** alanında değerlendirme kaydını gerçekleştiren çalışanın adını seçin.
7. **Satırlar** alanında koşul değerlendirmesinde ayarlanan değerlendirme satırlarının sayısını görürsünüz.
8. **Şablon** alanında koşul değerlendirmesi için bir şablon seçin. Şablonun adı **Ad** alanına otomatik olarak eklenir ve ilgili kayıt satırları **Koşul değerlendirme satıları** hızlı sekmesine eklenir.
9. **Notlar** hızlı sekmesine seçili koşul değerlendirmesiyle ilgili notları ekleyebilirsiniz.
10. Her koşul değerlendirme satırı için **Değer** alanında ölçüm verilerini ekleyin.
11. **Koşul değerlendirmesi satıları** hızlı sekmesinde > **Yorumlar** alanına seçili kayıt satırıyla ilgili bir yorum ekleyebilirsiniz. Bir satıra bir yorum eklerseniz **Yorum** onay kutusu otomatik olarak seçilir.

Kıymet üzerinde bir koşul değerlendirme kaydı yaptıktan sonra bir koşul değerlendirme raporunu yazdırabilirsiniz.

>[!NOTE]
>Ayrıca bir iş emrine de koşul değerlendirmesi kaydedebilirsiniz (**Kıymet yönetimi** > **Ortak** > **İş emirleri** > **Tüm İş emirleri** > **Koşul değerlendirmesi** düğmesi).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]