---
title: Düşürülebilir TDS sertifika numaralarını kaydetme
description: Bu makalede; belirli bir satıcı, müşteri veya genel muhasebe için alınan Kaynakta Kesilen Vergi (TDS) sertifikaları için sertifika numaralarını ve tarihlerini kaydetmek üzere Düşülebilir sertifikalar sayfasının nasıl kullanılacağı açıklanmaktadır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 513412e292167795fad9d80b68e6e5e14dbd13c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853270"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Düşürülebilir TDS sertifika numaralarını kaydetme

[!include [banner](../includes/banner.md)]

Bu makalede; belirli bir satıcı, müşteri veya genel muhasebe için alınan Kaynakta Kesilen Vergi (TDS) sertifikaları için sertifika numaraları ve tarihlerini kaydetmek üzere **Düşülebilir sertifikalar** sayfasının nasıl kullanılacağı açıklanmaktadır. TDS hareketleri için kaydedilen TDS sertifika numaralarını ve tarihlerini güncelleştirmek için bu sayfada **Sertifikayı güncelleştir** sayfasını (**Genel muhasebe \> Dönemsel \> Stopaj vergisi \>Güncelleştirme sertifikası**) kullanın. TDS sertifika numaralarını güncelleştirmeyi bitirdikten sonra, bunları kapatın.

TDS sertifika numaralarını ve tarihlerini kaydetmek için aşağıdaki adımları izleyin.

1. **Vergi \> Dolaylı vergi \> Stopaj vergisi \> Düşürülebilir sertifikaları**'na gidin.

    [![Düşürülebilir sertifikalar sayfası.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. **Düşürülebilir sertifikaları** sayfasında, **Vergi türü** alanında **TDS** seçeneğini belirleyin.
3. Bir kayıt oluşturmak için **Yeni**'yi seçin.
4. **Sertifika numarası** alanında, TDS sertifika numarasını girin.
5. **Hesap türü** alanında, TDS sertifikasının alındığı hesabın türünü seçin: **Satıcı**, **Müşteri** veya **Genel muhasebe**.
6. **Hesap** alanında, seçtiğiniz hesap türüne bağlı olarak satıcı, müşteri veya genel muhasebe hesap numarasını seçin. **Ad** alanı; satıcı, müşteri veya genel muhasebe hesabının adını gösterir.
7. **Sertifika tutarı** alanına TDS sertifikasının tutarını girin.
8. **Tarih** alanında, sertifika numarası için sertifika tarihini girin.
9. TDS sertifika numarası ve tarihinin güncelleştirildiği TDS hareketlerini görüntüleyebileceğiniz **Sertifika hareketleri** sayfasını açmak için **Sorgular**'ı seçin. Bu bilgiler, **Sertifikayı güncelleştir** sayfasında (**Vergi \> Beyannameler \> Stopaj vergisi \>Sertifikayı güncelleştir**) güncelleştirilebilir.

    **Sertifikayı güncelleştir** sayfası, her TDS hareketiyle ilgili olarak aşağıdaki bilgileri gösterir:

    - **Tarih** - TDS hareketinin deftere nakil tarihi.
    - **Fiş** – TDS hareketinin fiş numarasını görüntüler.
    - **Kaynak** – TDS hareketinin içinde oluşturulduğu modül.
    - **Hesap** – TDS hareketinin adına oluşturulduğu satıcı, müşteri veya genel muhasebe hesabı numarası.
    - **Ad** – TDS hareketinin adına oluşturulduğu satıcı, müşteri veya genel muhasebe hesabının adı.
    - **Tutar** – TDS'nin üzerinde hesaplandığı fatura tutarı.
    - **Vergi tutarı** – Hareket için hesaplanan TDS vergi tutarı.
    - **Sertifika tarihi** – TDS hareketi için güncelleştirilen TDS sertifika tarihi.
    - **Sertifika numarası** – TDS hareketi için güncelleştirilen TDS sertifika numarası.

10. **Düşürülebilir sertifikaları** sayfasında, **Sertifikayı güncelleştir** sayfasında TDS hareketlerinin güncelleştirmesini bitirdikten sonra TDS sertifika numarasını kapatmak için **Kapalı** onay kutusunu seçin.

    Sayfadaki tüm kayıtlar için **Kapalı** onay kutusunu seçmek için **Tümünü işaretle**'yi seçin.

    > [!NOTE]
    > **Kapalı** onay kutusunun seçili olduğu TDS sertifika numaraları, **Sertifikayı güncelleştir** sayfasında kullanılamaz.
