---
title: Kolaylaştırılmış çalışan girişi ve gezintisi
description: Çalışanlar için Dynamics 365 Talent veri girişi, geçmişte, etkin veya gelecekteki tüm çalışanlar için hızlı girişe izin verecek şekilde geliştirilmiştir. Basitleştirilmiş/birleştirilmiş bir gezinti modeli, ilgili bilgilere hızla ulaşmak ve gerekli güncelleştirmeleri yapmak için güncelleştirilmiştir.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent October 2019 update
ms.openlocfilehash: 35cceb97442b05abc243cf7341e0ce7a0d09c613
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915213"
---
# <a name="streamlined-employee-entry-and-navigation"></a>Kolaylaştırılmış çalışan girişi ve gezintisi

Dynamics 365 Talent, çalışan ve iş verilerinin etkili şekilde girişine olanak sağlar. Geçmiş, etkin ve gelecekteki çalışanlar ve yükleniciler için çalışma geçmişi bilgilerini hızlı şekilde güncelleştirebilirsiniz.

Ayrıca, hızlı bir şekilde ilgili bilgileri bulmak ve gerekli değişiklikleri yapmak için basitleştirilmiş bir gezinme deneyimini etkinleştirebilirsiniz. Bu işlevsellik artık tüm ortamlarda kullanılabilir. Bu özelliği etkinleştirmek için **Sistem yönetimi > özellik yönetimi > Yeni > Kolay personel girişi > Etkinleştir**'e gidin. Bu değişiklikler tüm kullanıcılar için etkinleştirilir. Bu seçeneği istediğiniz zaman kapatabilirsiniz.

## <a name="view-options"></a>Görünüm seçenekleri

Çalışanların ve yükleniciler grubunun herhangi bir bileşimini tek listeden seçmek için çalışan formundaki **Seçenekleri görüntüle** kullanabilirsiniz. Bu seçenekler, yasal varlıklar üzerindeki çalışanları veya şu anda oturum açmış olduğunuz yasal varlığı görüntülemenizi sağlar. Ayrıca, etkin, beklemede ve çıkan çalışanları da görüntüleyebilir ve sonuçları çalışan türüne göre (çalışan veya yüklenici) sınırlandırabilirsiniz. Gelişmiş güvenlik etkin ise, yalnızca erişim izni olan yasal varlıklardaki çalışanları ve yüklenicileri görürsünüz.

Liste görünümündeki sütunlar seçimlerinize göre değişiklik yapar. Örneğin, çıkan çalışan görüntülendikten sonra, sonlandırma tarihi ve neden kodları listede ek sütunlar olarak görüntüler. 

[![Görünüm seçenekleri](./media/Worker-view-option.png)](./media/worker-view-option.png)

## <a name="navigation-and-banner"></a>Gezinti ve başlık

Ana başlık, her çalışan için önemli bilgileri görüntüler. Etkin çalışanların başlığı aşağıdaki alanları görüntüler:

- **Ünvan**
- **Departman**
- **Pozisyon türü**
- **Çalışan türü**
- **Yönetici**
- **Tüzel kişilik**

Çıkan çalışanların başlığı aşağıdaki alanları görüntüler:

- **Çıkış tarihi**
- **Neden**

Bekleyen çalışanların başlığı aşağıdaki alanları görüntüler:

- **Ünvan**
- **Departman**
- **Pozisyon türü**
- **Yönetici**
- **Başlangıç tarihi**
- **Tüzel kişilik**

Çalışan sayfasının eylem bölmesi daha az seçenek içerecek şekilde yeniden düzenlenmiştir. Bilgiler şimdi aşağıdaki kategorilerde düzenlenmiştir: 

- İş
- Kişi
- Bırak
- Ücret
- Kazançlar
- Uyumluluk

Ek olarak, ana çalışan sayfasındaki yeni **bağlantılar** sekmesi kullanıcılara bir çalışanın ilgili tüm bilgilerine erişmek için merkezi bir konum sağlar.

Bu değişiklikler nedeniyle, bilgiler kullandığınızdan farklı bir konumda görünebilir. Örneğin, daha önce çalışan formunda görüntülenen bordro bilgileri artık **Ücret > Bordro**nun altındaki eylem bölmesinde görünür ve **kişisel bilgiler sekmesinde** **Daha fazla** düğmesi sık erişilmeyen alanları gizlemek için kullanılır.

[![Başlık](./media/Banner.png)](./media/Banner.png)

## <a name="work-history"></a>İş geçmişi

**Çalışma geçmişi** sekmesi, tüm tüzel kişiliklerin iş geçmişini gösterir ve çıkan, etkin ve bekleyen çalışanlar ve yükleniciler için kullanılabilir. Artık erişim izni olan tüzel kişilikler için tüm çalışma geçmişini bir seferde görüntüleyebilirsiniz. Ek olarak, veri bağlamını değiştirmeden her çalışma geçmişi girişi için bilgi düzenleyebilirsiniz. Tüm bilgileri doğrudan sayfada güncelleştirebilirsiniz. 

[![İş geçmişi](./media/Worker-work-history.png)](./media/Worker-work-history.png)

## <a name="position-history"></a>Pozisyon geçmişi

Ana çalışan sayfasındaki **pozisyonlar** sekmesi, geçmiş, şimdiki ve gelecekteki atamalar dahil olmak üzere kuruluş içinde bulunan tüm konumların tam görünümünü sağlar. Yine de, eylem bölmesindeki çalışanın konum geçmişine doğrudan gidebilirsiniz.

[![Pozisyonlar](./media/Worker-position-history.png)](./media/Worker-position-history.png)

