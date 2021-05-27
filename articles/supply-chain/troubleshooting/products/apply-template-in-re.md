---
title: Serbest bırakılan bir ürüne şablon uygulayamazsınız
description: Serbest bırakılan bir ürüne şablon uygulayamazsınız.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026976"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>Serbest bırakılan bir ürün oluşturmak için şablon uygulayamazsınız.

KB numarası: 4612097

## <a name="symptoms"></a>Belirtiler

**Yeni serbest bırakılan ürün** iletişim kutusunu kullanarak yeni bir serbest bırakılmış ürün oluşturduğunuzda, bir şablon seçebilirsiniz. Şablon, serbest bırakılan yeni ürünün birçok alanı için varsayılan ayarlar sağlamalıdır. Ancak, siz şablonu seçtikten sonra alanların bir kısmı veya tümü ayarlanamaz.

## <a name="cause"></a>Nedeni

Microsoft Dynamics 365 Supply Chain Management'ın birçok sayfası , bu sayfalarda gösterilen kayıtlar için başlangıç ayarlarını oluşturan bir şablon oluşturmanıza olanak sağlar. Eylem Bölmesinin **Seçenekler** sekmesinde **Kayıt bilgileri**'ni seçerek bu şablonlardan birini oluşturabilirsiniz. Ancak, serbest bırakılan ürünler birçok kayıt türünden çok daha karmaşıktır. Bir şablon oluşturmak için **Serbest bırakılan ürünler** sayfasında **Kayıt bilgileri**'ni seçebilir ve serbest bırakılan bir ürün oluşturduğunuzda bu şablonu seçebilirsiniz ancak şablon yeni serbest bırakılan ürün için beklenen alan değerlerini sağlamaz. Bu nedenle, serbest bırakılan ürünler için "kayıt bilgileri" şablonlarını kullanamazsınız. Bunun yerine, özel ürün şablonları oluşturmanız gerekir.

## <a name="resolution"></a>Çözünürlük

Ürün şablonu oluşturmak için, **Seçenekler** sekmesindeki **Kayıt bilgileri** düğmesini değil, Eylem Bölmesinin **Ürün** sekmesindeki **Şablon** menüsünü kullanın.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Eylem Bölmesinde, **Ürün** sekmesinde, **Yeni** grubunda, **Şablon** seçeneğini belirleyip , gerektiği şekilde **Kişisel Şablon oluştur** ya da **Paylaşılan şablon oluştur**'u seçin.
