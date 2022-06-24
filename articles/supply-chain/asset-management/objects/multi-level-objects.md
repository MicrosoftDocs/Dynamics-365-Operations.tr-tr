---
title: Çok düzeyli kıymetler
description: Bu makalede, çok düzeyli kıymetleri oluşturma ve silme açıklanmaktadır.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34ab83c9f9673c39006b3985ebaac9e17a45da82
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908786"
---
# <a name="multi-level-assets"></a>Çok düzeyli kıymetler

[!include [banner](../../includes/banner.md)]

 

Bu makalede, çok düzeyli kıymetleri oluşturma ve silme açıklanmaktadır. Hiyerarşik ağaç yapısında kıymetler ve ilgili alt kıymetler oluşturabilirsiniz. Bu şekilde kıymetler arasındaki ilişkileri ve bağımlılıkları gösterebilirsiniz. Bakım işleri, ağaç yapısının tüm düzeyleriyle ilgili olabilir. İstatistikler tek bir düzey veya tüm alt kıymet düzeylerinin toplamı olarak da oluşturulabilir.

**Tüm Kıymetler** listesi sayfasında (**Kıymet yönetimi** \> **Ortak** \> **Kıymetler** \> **Tüm kıymetler**), **Kıymet** sütunu kıymetleri hiyerarşik düzende listeler. **Üst Öğe** sütunu ilgili üst öğe gösterilir. Ayrıca kıymetler ve alt kıymetler zaten oluşturulmuşsa **İlgili bilgiler** bölmesindeki **Kıymet ağacı** bölümü kıymetleri bir ağaç yapısında gösterir.

Bir kıymet oluşturma hakkında bilgi için bkz. [Kıymet oluşturma](../objects/create-an-object.md). Bir alt kıymet oluşturmak için **Genel** hızlı sekmesinin **Üst Öğe** alanındaki üst kıymeti seçin.

## <a name="copy-an-asset-or-asset-structure"></a>Kıymeti veya kıymet yapısını kopyalama

Şirketinizde birkaç benzer kıymet yapısı varsa, bunları hızla oluşturmak için Kıymet Yönetimi'ndeki Kopyala işlevini kullanabilirsiniz.

1. **Kıymet yönetimi** \> **Ortak** \> **Kıymetler** \> **Tüm kıymetler** öğesini seçin.
2. **Tüm kıymetler** listesi sayfasında kopyalanacak kıymeti seçin. Örneğin alt kıymetler dahil olmak üzere tüm kıymet yapısını kopyalamak istiyorsanız bir üst kıymeti seçin.
3. **Kıymeti kopyala**'yı seçin. **Kopyalama kaynağı** bölümünde, **Kıymet** alanı liste sayfasında seçtiğiniz kıymete ayarlanır.
4. **Kopyalama hedefi** bölümündeki **Kıymet** alanında yeni kıymetin adını girin.
5. Oluşturduğunuz kıymet mevcut kıymet yapısının parçasıysa **Üst kıymet** bölümündeki **Kıymet** alanında bir üst kimlik seçin.
6. **Tamam**'ı seçin. Yeni kıymet yapısı **Tüm kıymetler** listesi sayfasında gösterilir. Kopyaladığını kıymetle ilgili tüm kıymet öznitelikleri, bakım planları ve bakım sıraları yeni kıymete veya kıymet yapısına aktarılır.

Bir kıymet yapısını kopyaladığınızda yeni yapıdaki alt kıymetler kopyaladığınız alt kıymetlerle aynı ada sahip olur. Kopyalama işlemi tamamlandıktan sonra bir kıymetin adını ve diğer ayarlarını kolayca değiştirebilirsiniz. **Tüm kıymetler** listesi sayfasındaki kıymeti ve ardından **Düzenle** düğmesini seçin.

> [!NOTE]
> Bir kıymeti veya kıymet yapısını kopyaladığınızda yeni kıymetlerin yaşam döngüsü durumu kıymetler için ilk yaşam döngüsü durumu olarak tanımladığınız duruma sıfırlanır. İşlem yapılacak yerleşim varsayılan işlem yapılacak yerleşime sıfırlanır.

## <a name="delete-an-asset-or-asset-structure"></a>Kıymeti veya kıymet yapısını silme

Bir kıymetin ilgili alt kıymetleri varsa kıymetler üzerinde kayıtlı bakım talepleri, iş emri işleri, arıza kayıtları veya koşul değerlendirmeleri yoksa kıymeti silebilirsiniz.

1. **Tüm kıymetler** listesi sayfasında silinecek kıymeti seçin.
2. **Sil**'i seçin.

> [!NOTE]
> Bir kıymeti bu yordamı kullanarak silemezseniz silme işlemini gerçekleştirmenin bir diğer yolu da bir kıymet yaşam döngüsü durumunu bu amaçla ayarlamaktır. Örneğin **Kıymet yaşam döngüsü durumlar** sayfasında **Iskarta** veya **Silindi** yaşam döngüsü durumu ayarlayabilirsiniz.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]