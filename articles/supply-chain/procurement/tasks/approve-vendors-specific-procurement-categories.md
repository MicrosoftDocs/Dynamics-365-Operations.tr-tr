---
title: Belirli tedarik kategorileri için satıcıları onaylama
description: Bu makale, Dynamics 365 Supply Chain Management'ta belirli tedarik kategorileri için satıcıların nasıl onaylanacağını açıklamaktadır.
author: GalynaFedorova
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb6861c1cfbc7702fae74b4aa97fe618b50ac0bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903999"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>Belirli tedarik kategorileri için satıcıları onaylama

[!include [banner](../../includes/banner.md)]

Bu makale, Dynamics 365 Supply Chain Management'ta belirli tedarik kategorileri için satıcıların nasıl onaylanacağını açıklamaktadır. Satınalma talebi oluşturulduğunda satınalma ilkelerinin nasıl ayarlandığına bağlı olarak onaylanan veya tercih edilen bir satıcıyı seçmek gerekebilir. Bu prosedür belirli bir tedarik kategorisi için bir satıcının onaylanan veya tercih edilen olduğunu nasıl belirleyeceğinizi gösterir. Bu görev genellikle bir tedarik profesyoneli tarafından gerçekleştirilir. Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.

1. Gezinti Bölmesi'nde **Modüller > Tedarik ve kaynak atama > Satıcılar > Tüm satıcılar**'a gidin.
2. Bir kategori için onaylanan veya tercih edilen satıcı olarak ayarlamak istediğiniz satıcıyı seçin.
3. Eylem Bölmesinde, **Genel**'i seçin.
4. **Kategoriler**'i seçin.
5. **Kategori ekle**'yi seçin.
6. **Kategori** alanından **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**'i seçin.
7. **Satıcı kategorisi durumu** alanından **Tercih edilen**'i seçin. Bir kategori için birden fazla tercih edilen satıcı belirlemek mümkündür.  
8. **Kaydet**'i seçin.
9. Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Tedarik kategorileri**'ne gidin.
10. Ağaçtan, **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**'i seçin.
11. **Satıcılar** bölümünü genişletin. Seçtiğiniz satıcı Ofis ve masa aksesuarları kategorisi için tercih edilen satıcı olarak görünüyorsa işaretleyin. Bu prosedürü görev kılavuzu olarak çalıştırıyorsanız satıcılar listesine inebilmek için **Kilidi aç** düğmesini seçebilirsiniz.  Tercih edilen ve onaylanan satıcıları bu sayfada eklemek mümkündür.  
12. Ağaçta **OFFICE AND DESK ACCESSORIES**'i genişletin ve **Makaslar**'ı seçin.
13. **Ana kategoriden satıcıları devral:** alanından **Hayır**'ı seçin.
14. **Ana kategoriden satıcıları devral:** alanından **Evet**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]