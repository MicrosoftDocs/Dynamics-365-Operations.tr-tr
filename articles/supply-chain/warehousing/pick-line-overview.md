---
title: Bir mobil cihaz menü öğesini malzeme çekme satırı özeti sağlayacak şekilde ayarlama
description: Bu konu, bir mobil cihazda ambar çalışmasını işleyen ambar çalışanlarına tüm iş satırlarının listesinin nasıl tanımlanacağını açıklar. Bu özellik, malzeme çekme sırasını en iyi duruma getirebilmek için bir iş emrindeki çekme satırlarının genel görünümüne gerek duyan ambar çalışanları için kullanışlı olabilir.
author: Mirzaab
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d3a8972c5d2f4c52dddef458ebd6079118cadfe
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901934"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Bir mobil cihaz menü öğesini malzeme çekme satırı özeti sağlayacak şekilde ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, malzeme çekme işini işlemek için kullanılan mobil cihaz menü ögelerinin çekme satırı genel bakışla ilgili seçeneklerini nasıl yapılandırılacağını açıklar. Çekme satırı genel bakışı ambar işçileri, geçerli görevlerinden ilgili tüm iş satırlarının listesinden seçim yapmanızı sağlar. Bu özellik, çalışanların malzeme çekme sıralarını en iyi duruma getirmesine yardımcı olur. Bu özellik, çalışanların sabit bir zamanda satırlar arasında dolaşmasına izin veren standart **Atlama** düğmesini değiştirecek seçenekler sunar. (Ancak, bu düğmeyi kullanma seçeneği hala bulunur.)

Yöneticiler her bir menü öğesini, Ambar Yönetimi mobil uygulamasının çekme satırı özetini nasıl, ne zaman ve nerede sunduğunu kontrol edebilecek yapılandırabilir.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>İş çekme satırı özeti özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** _Ambar yönetimi_
- **Özellik adı:** _İş çekme satırı özeti_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Tüm iş satırlarının listesini göstermek için menü öğelerini yapılandırma

Bir mobil cihaz menü öğesini malzeme çekme satırı özeti sağlayacak şekilde ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Malzeme çekme işiyle ilişkili menü ögesini seçin veya oluşturun ve aşağıdaki değerleri ayarlayın:

    - **Mod:** *İş*
    - **Mevcut işi kullan:** *Evet*
    - **Yöneten:** *Kullanıcı yönlendirmesinde* veya *Sistem yönlendirmesinde*

    Menü ögeleri oluşturma ve **Mobil cihaz menü öğeleri** sayfasında bulunan çeşitli ayarları kullanma hakkında daha fazla bilgi için bkz. [Ambar işi için mobil cihazları ayarlama](configure-mobile-devices-warehouse.md).

1. **Genel** hızlı sekmesinde, **Çalışma satırı listesini göster** alanını aşağıdaki değerlerden birine göre ayarlayarak özelliği yapılandırın:

    - **Yalnızca talep üzerine göster**: Çalışanlar Ambar Yönetimi mobil uygulamasında **Atla** düğmesini seçerek çekme satırı listesini görüntülemeyi seçebilirler.
    - **Her bir çekmenin başlangıcında göster**: Çalışanlar, bir çekme satırını her başlattıklarında veya tamamladıklarında listeye bakar. Ambar Yönetimi mobil uygulamasında **Atla** düğmesini seçerek listeyi yeniden görüntüleyebilirler.
    - **Yalnızca ilk çekmenin başlangıcında göster**: Çalışanlar, listeyi her satırdan sonra değil, her yeni çekme işi başlattıklarında görür. Ambar Yönetimi mobil uygulamasında **Atla** düğmesini seçerek listeyi yeniden görüntüleyebilirler.
    - **Hiçbir zaman gösterme**: Ambar Yönetimi mobil uygulamasında standart **Atla** düğmesi görünür ve iş satırı listesinin görünümü kapalıdır. **Atla** düğmesi, işçilerinin, her seferinde bir satır içinde, sabit bir sırada dolaşmasına olanak tanır. Tüm satırlar işlenene kadar, listede gereksinim duydukları kadar çok sayıda döngü de yapabilirler.

1. Eylem bölmesinde, **Kaydet**'i seçin.

    **Çalışma satırı listesini göster** alanını *Hiçbir zaman gösterme* değeri dışında herhangi bir değere ayarlarsanız, Eylem Bölmesi'ndeki **Alan listesi** düğmesi kullanılabilir duruma gelir.

1. Eylem Bölmesi'nde, **Alan listesi** öğesini seçin.
1. **Alan listesi** sayfasında, listedeki her satır için Ambar Yönetimi mobil uygulamasının gösterdiği bilgileri yapılandırın.

    - **Birincil denetim** alanı her zaman *LineNum* olarak ayarlanır. Bu nedenle, listedeki her satır bir satır numarasıyla başlar.
    - Gereksinim duyduğunuzda, yedi taneye kadar ek görüntüleme alanı eklemek için kalan **Görüntüleme alanı** alanlarını kullanın. Her **Görüntüleme alanı** alanında, bir iş satırı alanının adını seçin. Böylece her satır, o alan için bir değer gösterir. Değerler, buradan seçtiğiniz sırada gösterilir. Yedi değere ihtiyacınız yoksa, **Görüntüleme alanı** alanlarından bazılarını boş bırakabilirsiniz.

1. Eylem Bölmesi'nde **Kaydet**'i seçin ve ardından **Alan listesi** sayfasını kapatın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]