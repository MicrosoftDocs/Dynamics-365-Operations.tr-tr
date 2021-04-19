---
title: Projeler ve servis sözleşmeleri için tümleştirme
description: Servis anlaşmalarıyla ve servis anlaşması satırlarıyla çalıştığınızda, Proje yönetimi ve muhasebe bölümünün aşağıdaki alanlarında belirlenmiş verileri kullanırsınız.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9855915bd4d1f8ebb0c73bf53e7032af4972c45
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831588"
---
# <a name="integration-for-service-agreements-and-projects"></a>Projeler ve servis sözleşmeleri için tümleştirme 

[!include [banner](../includes/banner.md)]


Servis anlaşmalarıyla ve servis anlaşması satırlarıyla çalıştığınızda, **Proje yönetimi ve muhasebe** bölümünün aşağıdaki alanlarında belirlenmiş verileri kullanırsınız.

## <a name="project-prices"></a>Proje fiyatları

Bir servis anlaşması hareketi için satış fiyatı ve maliyeti, servis anlaşmasına eklenen projeye uygulanan maliyet fiyatı kurulumundan türetilir. Maliyet ve satış fiyatları proje, çalışan ve kategoriye göre ayarlanabilir. 

## <a name="project-validation"></a>Proje doğrulama

Servis anlaşması satırındaki seçilebilecek projeler, çalışanlar ve kategoriler **Proje yönetimi ve muhasebe**'deki doğrulamaya ayarıyla sınırlandırılabilir. Doğrulama ayarını kullanarak çalışanları, projeleri ve kategorileri erişim denetimi için bir araya getirebilirsiniz. 

## <a name="project-line-properties"></a>Proje satırı özellikleri

Bir satır özelliği, bir servis anlaşması satırı için otomatik olarak girilir.

Satır özellikleri **Proje yönetimi ve muhasebe**'deki **Satır özellikleri** formunda oluşturulur. Bir servis anlaşmasına girilen satır özelliği servis anlaşması için seçilen projeye iliştirilir ve daha sonra servis anlaşması satırı tarafından devralınır. 

## <a name="default-offset-accounts"></a>Varsayılan mahsup hesaplar

Gider hareketi girerseniz, varsayılan gider mahsup hesabı hareket için otomatik olarak seçilir. Varsayılan gider hesabı geçerli servis anlaşmasına eklenen proje için ayarlanır.

## <a name="project-categories"></a>Proje kategorileri

Servis anlaşması satırları için kullanılabilecek kategoriler **Proje yönetimi ve muhasebe** bölümündeki **Proje kategorileri** formunda belirlenir. 

> [!NOTE]
> <P><STRONG>Proje kategorileri</STRONG> formundaki <STRONG>Proje</STRONG> sekmesinde <STRONG>Günlüklerde etkin</STRONG> onay kutusu seçili olan kategoriler seçilebilir. Ancak, <STRONG>Proje yönetimi ve muhasebe parametreleri</STRONG> formundaki <STRONG>Günlükler</STRONG> sekmesinde <STRONG>Etkin olmayan kategoriler</STRONG> onay kutusu seçiliyse tüm kategoriler seçilebilir.</P>

## <a name="project-parameters"></a>Proje parametreleri

**Proje yönetimi ve muhasebe parametreleri** formundaki **Günlükler** sekmesinde **İşine son verilen çalışanlar** alanı seçiliyse, **Servis sözleşmeleri** ve **Servis siparişleri** formlarında etkin olmayan ve etkin olan çalışanları seçebilirsiniz.

Ayrıca, servis siparişi satırlarına başlangıç ve bitiş saatleri girmek için **Servis siparişleri** formundaki **Proje** sekmesinde bulunan **Başlangıç zamanı** ve **Bitiş zamanı** alanlarını etkinleştirebilirsiniz.

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>Servis siparişleri için başlangıç ve bitiş zamanı özelliğini etkinleştirme

1.  **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Proje yönetimi ve muhasebe parametreleri**'ne tıklayın.

2.  **Günlükler** sekmesine tıklayın ve sonra **Başlangıç/bitiş zamanlarını göster** onay kutusunu seçin.

3.  **Proje yönetimi ve muhasebe** \> **Kurulum** \> **Günlükler** \> **Günlük adları**'na tıklayın.

4.  Servis siparişine iliştirilen günlük adını seçin.

5.  **Genel** sekmesine tıklayın ve sonra **Başlangıç/bitiş zamanlarını göster** onay kutusunu seçin.


> [!NOTE]
> <P><STRONG>Servis yönetimi parametreleri</STRONG> formundaki <STRONG>Günlükler</STRONG> sekmesinde yer alan <STRONG>Saat</STRONG> alanında servis siparişi için günlük adını seçin.</P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]