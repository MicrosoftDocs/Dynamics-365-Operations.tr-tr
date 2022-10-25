---
title: Talep Temelli Malzeme Gereksinimleri Planlaması (DDMRP) genel bakışı
description: Bu makalede, arz ve talebin ayırma noktasına dayanan bir planlama metodolojisi olan Talep Temelli Malzeme Gereksinimleri Planlaması (DDMRP) hakkında bilgi sağlanmaktadır.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 31b45fdb92cf8a590ff77104f0c8015fb4d329d5
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689501"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Talep Temelli Malzeme Gereksinimleri Planlaması (DDMRP) genel bakışı

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Şirketler yıllardır bir ürünü üretmek üzere gerekli malzemeleri ve bileşenleri hesaplamak için bir sistem olarak Malzeme Gereksinimleri Planlaması (MRP) kullanmışlardır. Ancak artık tedarik zincirleri değişti. Parçalar, giderek daha fazla yurt dışından tedarik edildiğinden daha uzun sağlama süreleri vardır. Bu nedenle, birçok şirket ne kadar envanter stoklayacaklarını bilmediklerinden stok eksiği veya stok fazlası yaşadığını bildirmiştir. Ayrıca daha fazla piyasa dalgalanması (bazen yanlış tahminler) vardır ve müşteriler kısa sağlama süresinde ürünler talep etmektedir. Bu nedenle, tüm dünyada tedarik zinciri eksiklikleri yaşanmaktadır. Ayrıca, MRP araçları planlamacılara sıklıkla yapacakları binlerce eylem sunar. Bu nedenle, neye odaklanılacağını bilmek zor. Genellikle, bu sorunların çoğuna yönelik çözüm, Talep Temelli Malzeme Gereksinimleri Planlamasına (DDMRP) geçmektir.

DDMRP, arz ve talebin birbirinden ayrılmasına dayanan bir planlama metodolojisidir. Bu ayrılma, ayırma noktası maddelerini ayarlayarak elde edilir. Bu kalemler için, doğru miktarda stok tutulduğundan emin olmak için arabellekler korunur. Arz ve talebin birbirinden ayrılması "kamçı etkisinin" önlenmesine yardımcı olur, çünkü değişkenlik zincirden geçmez. *(kamçı etkisi* perakende seviyesindeki talepteki küçük dalgalanmaların toptan, distribütör, üretici ve hammadde tedarikçisi seviyelerinde aşamalı olarak daha büyük talep dalgalanmalarına neden olabileceğini ifade eder.) Her bir arabellek, bir parçanın ortalama kullanımını kapsamayı amaçlamaktadır ve ayrıca talep artışlarını kapsayacak şekilde ayarlanabilir.

DDMRP'nin, müşteri tolerans sürelerinin toplam sağlama sürelerinden daha kısa ve değişken ortamlar için değerli bir planlama metodolojisi olduğu kanıtlanmıştır.

## <a name="the-five-components-of-ddmrp"></a>DDMRP'nin beş bileşeni

DDMRP'nin beş sıralı bileşeni (adımları) vardır. İlk üç bileşen, esas olarak, talep odaklı bir malzeme gereksinimleri planlama modelinin ilk ve gelişen yapılandırmasını tanımlar. Son iki bileşen, metodolojinin günlük işlemini tanımlar.

1. **[Stratejik stok konumlandırma](ddmrp-inventory-positioning.md)** – Tedarik zinciri ağındaki ayırma noktalarını tanımlayın. Ayırma noktaları, izleyeceğiniz ve yenileyeceğiniz bir stok arabelleği yerleştirdiğiniz tedarik zincirinizin belirli noktalarıdır.
2. **[Tampon profiller ve düzeyler](ddmrp-buffer-profile-and-levels.md)** – Her bir ayırma noktası için, arabellek boyutlarını (minimum miktar, maksimum miktar ve yeniden sipariş noktası) ve yeniden sipariş miktarını belirleyin.
3. **[Dinamik arabellek düzeltmeleri](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** – Değişen işletim parametrelerine veya gelecekteki planlanan olaylara göre arabellek seviyelerini ayarlayın.
4. **[Talep temelli planlama](ddmrp-planning.md)** – Gerektiği gibi tedarik siparişleri oluşturun. Üretim siparişlerini, satınalma siparişlerini ve stok transfer siparişlerini içeren tedarik siparişleri
5. **[Kesinlikle işbirlikçi ve görünür yürütme](ddmrp-visual-and-collaborative-execution.md)** – Görselleştirme yardımıyla tedarik siparişlerini çalıştırın.

DDMRP genellikle çok seviyeli malzeme listesine (BOM) sahip üreticiler tarafından kullanılır. Ancak, dağıtım ve perakende ağlarına da uygulanabilir.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management'ta DDMRP

DDMRP, Microsoft Dynamics 365 Supply Chain Management dahildir ve ek lisans ücreti gerektirmez. Supply Chain Management'ta, mevcut **Master planlama** modülüne DDMRP işlevi eklenmiştir. Ancak, Planlamayı En İyi Duruma Getirme Eklentisini kullanmanızı gerektirir. 

DDMRP, Supply Chain Management'taki mevcut planlama kurulumlarıyla tümleşiktir ve işletmeniz için doğru planlama yapılandırmasına ulaşmak için bu kurulumlarla birlikte kullanılır. Dönemden tamamen farklı yeni bir karşılama kodu tarafından kontrol edilir, min/maks, gereksinim v.s. Bu yeni bir modül değil ve mevcut planlama işlevini değiştirmez. Ancak, size kullanmak için daha fazla işlevsellik sağlar.
