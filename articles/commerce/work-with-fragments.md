---
title: Parçalarla çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d92b9077f8584bfa0710bbaacbc7caa3220baa4a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698108"
---
# <a name="work-with-fragments"></a>Parçalarla çalışma 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Parçalar, tüm sitenizde yeniden kullanılması gereken modül yapılandırmaları için merkezi bir yazma deneyimine olanak sağlar. Örneğin, üstbilgiler, altbilgiler ve başlıklar birçok sayfada paylaşıldıklarından, genellikle parçalar halinde yapılandırılır. Parçaları sitenizdeki diğer sayfalara eklenebilen minyatür Web sayfaları olarak düşünebilirsiniz. Parçaların kendi yaşam döngüsü vardır. Başka bir deyişle bunlar, yazma araçlarında bağımsız varlıklar olarak oluşturulur, başvurulur, güncellenir ve silinir.

Parçalar yapılandırıldıktan sonra, site yapınızda modüllerin kullanılabileceği her yerde kullanılabilirler. Parçalar sayfalarda, mizanpajlarda, şablonlarda ve diğer parçalarda başvurulabilir.

> [!NOTE]
> Parçalar, diğer parçaların içinde en fazla yedi düzeye kadar iç içe geçmiş olabilir.

Örneğin, sitemizde birçok sayfada dönemsel olay yükseltmek istiyorsanız, bir parça kullanabilirsiniz. Yeni parça oluşturma işlemindeki ilk adım, başlatmak istediğiniz modül türünü seçmektir. Bu örnekte, bir kahraman modülünden parça oluşturabilirsiniz.

> [!NOTE]
> Parçalar herhangi bir modül türünden oluşturulabilir.

Bundan sonra, hero parçacığını özel tanıtım içerikleriniz ile konfigüre edebilirsiniz. Ayrıca, bunu gereksinim duyduğunuz şekilde yerelleştirebilirsiniz. Yeni tek başına kahraman parçası daha sonra, siteniz genelinde önceden yapılandırılmış bir modül olarak tüketilebilir. Bunu şablonlara, belirli sayfalara veya kahramanı modüllerini içerebilecek diğer parçalara kolayca ekleyebilirsiniz.

Parçanın eklendiği tüm yerler, oluşturduğunuz Merkez kahraman parçasına yapılan referanslardır. Değişiklikleri parçalara yayımlarsanız, bu değişiklikler derhal site genelinde referans alınan tüm yerlere yansıtılır. Bu nedenle, parçalar bir sitede modül konfigürasyonlarını tekrar kullanmak ve merkezi olarak yönetmek için güçlü ve etkili bir yol sağlar. Bunları etkili şekilde kullanarak, size önemli ölçüde yükseltebilir ve Site içeriğiyle ilgili maliyeti azaltmaya yardımcı olabilirsiniz.

Aşağıdaki şekil, bir e-ticaret sitesinde paylaşılan modül konfigürasyonlarını merkezileştirmek için parçaların nasıl kullanılabileceğini göstermektedir.

![Aşağıdaki şekil, bir e-ticaret sitesinde paylaşılan modül konfigürasyonlarını merkezileştirmek için parçaların nasıl kullanılabileceğini göstermektedir.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Parça oluştur

Yeni bir parça oluşturabilir veya varolan bir modül konfigürasyonunu parça olarak kaydedebilirsiniz.

### <a name="create-a-new-fragment"></a>Yeni bir parça oluşturun.

Bir yeni parça oluşturmak için şu adımları izleyin.

1. Soldaki gezinti bölmesinde **Parçalar** seçin.
1. **Yeni Sayfa Parçası**'nı seçin. Kullanılabilen tüm modül türlerini gösteren bir iletişim kutusu görüntülenir. Daha önce belirtildiği gibi, parçalar herhangi bir modül türünden oluşturulabilir.
1. Parçanız için bir modül türü seçin ve sonra **Tamam**'ı seçin.

    > [!TIP]
    > Genel bir konteyner modülü türü seçerek parçanız daha sonra güncelleştirmeniz ve yapılandırmanız gerektiğinde en iyi esnekliği elde edebilirsiniz.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Varolan bir modül konfigürasyonunu parça olarak kaydet

Önceden yapılandırılmış bir modülü yeniden kullanılabilir parçaya dönüştürmek için aşağıdaki adımları izleyin.

1. Bir parçaya dönüştürmek istediğiniz modülü içeren sayfayı veya şablonu açın.
1. Soldaki anahat bölmesinde, modülün adının yanında üç nokta düğmesini (**...**) seçin ve **Parça olarak kaydet** seçin. İletişim kutusu görüntülenir.
1. Parça için bir ad ve meta veri girin.
1. Modül konfigürasyonunu diğer sayfalara eklenebilecek bir parça olarak kaydetmek için **Tamam**'ı seçin.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Sayfaya parça ekleme, kaldırma veya düzenleme

Aşağıdaki yordamlarda parçaların nasıl ekleneceği, kaldırılacağı ve düzenleneceği açıklanmaktadır.

### <a name="add-a-fragment"></a>Parça ekle

Bir sayfaya parça eklemek için bu adımları izleyin.

1. Soldaki anahat bölmesinde, alt modüllerin eklenebileceği bir konteyner veya yuva seçin.
1. Konteyner veya yuvanın adının yanındaki üç nokta düğmesini seçin ve **parça Ekle**'yi seçin. İletişim kutusu görüntülenir.

    > [!NOTE]
    > Bir konteyner veya yuva yeni alt modülleri desteklemiyorsa, **Parça Ekle** seçeneği kullanılamaz.

1. İletişim kutusunda, eklenecek bir parça arayıp seçin. Listelenmiş parça listelenmezse, önce seçilen konteyner veya yuvanın desteklediği bir modül türünden bir parça oluşturmanız gerekebilir.
1. Seçili parça sayfanızdaki seçili konteynere veya yuvaya eklemek için **Tamam**'ı seçin.

> [!NOTE]
> Bir konteynerde veya bir yuvada izin verilen modüller, sayfa şablonu veya modüllerin kendi tanımları tarafından tanımlanır.

### <a name="remove-a-fragment"></a>Parça kaldırma

Sayfada yuva veya konteynerden parça kaldırmak için bu adımları izleyin.

1. Soldaki anahat bölmesinde, kaldırılacak parçanın adının yanında üç nokta düğmesini seçin ve çöp tenekesi düğmesini seçin.
1. Parçayı kaldırma isteğinizi onaylamanız istendiğinde, **tamam**'ı seçin.

> [!NOTE]
> Sayfadan bir parçayı kaldırdığınızda, yalnızca bu sayfadan gelen başvuruyu kaldırırsınız. Sitenizden parçayı **silmeyin**. Sitenizdeki parçaları silmek için, parça denetçisi Kullanıcı arabirimini (UI) kullanmanız gerekir. Bir sitedeki parçaları yalnızca herhangi bir sayfa, şablon veya başka parçalar tarafından başvurulmuyorsa silebilirsiniz.

### <a name="edit-a-fragment"></a>Parça Düzenle

Parçaları düzenlemek için, parça düzenleyici kullanıcı arabimirni kullanmalısınız. Bu kısıtlama tasarımdan kaynaklanır. Yazarların belirli bir sayfa için modülleri düzenleme işlemini, birçok sayfada paylaşılabilecek parça düzenleme işlemi ile karıştıradığından emin olmanıza yardımcı olur.

Bir parça düzenlemek için şu adımları izleyin.

1. Soldaki gezinti bölmesinde **Parçalar** seçin.
1. **Parçalar** altında düzenlenecek parçayı seçin.
1. Parçanın modül özelliklerini ve yapısını gereksinim duyduğunuz şekilde Düzenle. İşlem, düzenleme modüllerinin sayfa düzenleyici görünümde düzenlenmesi işlemine benzer.

Bir parçayı sayfada, şablonda veya üst parçada seçerek ve sağdaki Özellikler bölmesinde **parça Düzenle** 'yi seçerek düzenleyebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Şablonlarla çalışma](work-with-templates.md)

[Önceden ayarlanmış düzenlerle çalışma](work-with-layouts.md)
