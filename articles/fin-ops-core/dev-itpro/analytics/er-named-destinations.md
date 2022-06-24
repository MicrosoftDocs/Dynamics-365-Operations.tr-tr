---
title: Yazdırma yönetimi kaydına özel ER hedeflerini yapılandırma
description: Bu makalede, giden belgeler oluşturmak üzere yapılandırılan bir Elektronik raporlama (ER) biçimi için yazdırma yönetimi kaydına özel hedeflerin nasıl yapılandırılacağı açıklanmaktadır.
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2972dc6a0b373cbc63b811c01ef7a5538810edbb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872727"
---
# <a name="configure-print-management-record-specific-er-destinations"></a>Yazdırma yönetimi kaydına özel ER hedeflerini yapılandırma

[!include [banner](../includes/banner.md)]

Bu makalede, Sistem Yöneticisi veya Alacak Hesapları Görevlisi rolüne sahip bir kullanıcının aşağıdaki görevleri nasıl gerçekleştirebileceği açıklanmaktadır:

- Serbest metin faturaları oluşturan bir ER çözümü için adlandırılmış [Elektronik raporlama (ER)](general-electronic-reporting.md) hedeflerini yapılandırın.
- Tek bir [baskı yönetimi](document-reporting-services.md) kaydına bir ER hedefi atayın.

Yordamlar, USMF şirketinde tamamlanabilir. Kodlama gerekmez.

## <a name="introduction"></a>Giriş

Giden belge oluşturmak üzere kullanılan bir ER [biçimi](general-electronic-reporting.md) [yapılandırmasının](general-electronic-reporting.md#Configuration) dosya çıkış bileşenindeki her klasör için [hedefleri](electronic-reporting-destinations.md) yapılandırabilirsiniz. Bu türde bir ER biçimi çalıştırdığınızda uygun erişim haklarına sahipseniz çalışma zamanında yapılandırılmış hedef ayarlarını da değiştirebilirsiniz.

Microsoft Dynamics 365 Finance **sürüm 10.0.17 ve sonrasında**, kullanıcıların bu ER biçimini çalıştırarak gerçekleştirdikleri eylemi belirtmek üzere ER biçimi için bir eylem kodu [ayarlanabilir](er-apis-app10-0-17.md). Örneğin, **Alacak hesapları** modülündeki yazdırma yönetimi ayarlarında, serbest metin faturası gibi belirli iş belgelerini oluşturan bir ER biçimi seçebilirsiniz. Daha sonra, faturanın önizlemesini görmek için **Görüntüle**'yi veya faturayı yazıcıya göndermek için **Yazdır**'ı seçebilirsiniz. Çalışma zamanında çalışan ER biçimi için bir eylem geçirilirse [farklı kullanıcı eylemleri için farklı ER hedefleri yapılandırabilirsiniz](er-action-dependent-destinations.md).

Finance **sürüm 10.0.21 ve sonrasında**, bir ER biçimi için adlandırılmış bir hedef [ayarlanabilir](er-apis-app10-0-21.md) ve bu ER biçimi çalıştırıldığında, işlenen yazdırma yönetimi kaydına atanabilir. Örneğin **Alacak hesapları** modülünde, yazdırma yönetimi ayarlarında aşağıdaki eylemleri gerçekleştirmek için **Orijinal** kaydı yapılandırmak istiyorsunuz:

- Bir ER biçimi çalıştırın.
- Oluşturulan faturayı bir müşteriye e-posta ile gönderin.
- Aynı biçimi çalıştırmak için **Kopya** kaydını yapılandırın.
- Faturanın bir kopyasını bir ağ yazıcısına yazdırın.

Bu durumda, çalışmakta olan ER biçimi için farklı ER hedefleri yapılandırmanız ve farklı yazdırma yönetimi kayıtları için hedefler seçmeniz gerekir.

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce, [Özellik yönetimi](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) çalışma alanında **Yazdırma yönetimi öğesi başına ER hedeflerinin ayarlanmasına izin ver** özelliği etkinleştirilmelidir. Geçerli Finance kurulumunda adlandırılmış ER hedeflerinin yapılandırılmasına izin vermek ve [yeni](er-apis-app10-0-21.md) ER API'sini etkinleştirmek için kaynak kodu da değiştirilmelidir.

Ek olarak, **Serbest metin faturası (Excel)** ER yapılandırması, Finance kurulumunuza [içeri aktarılmalıdır](er-download-configurations-global-repo.md).

## <a name="configure-a-new-er-destination"></a>Yeni bir ER hedefini yapılandırma

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. **US-001** müşteri hesabı için bir fatura seçin.
3. **Serbest metin faturası** sayfasında, **Fatura** sekmesinde, **Yazdırma yönetimi** grubunda **Yazdırma yönetimi**'ni seçin.
4. **Yazdırma yönetimi kurulumu** sayfasında, **Modül - alacak hesapları** \> **Belgeler** \> **Serbest metin faturası**'nı genişletin, **Orijinal** kaydı seçin ve ardından şu adımları izleyin:

    1.  Seçilen kaydın geçerli ayarlarını inceleyin:
        -   **Rapor biçimi** alanında varsayılan SSRS raporu olan **FreeTextInvoice.Report** seçilir.
        -   **\<Default\>** adı, atanan SSRS raporu için özel bir hedef seçilmediğini bildiren **Hedef** alanında gösterilir. 
    2.  **Rapor biçimi** alanında, **Serbest metin faturası (Excel)** ER biçimi yapılandırmasını seçin.
        -   **Hedef** alanının adı, **Hedef adı** olarak değiştirilir.
        -   **\<No named destination\>** adı, atanan ER biçimi için seçilmiş bir adlandırılmış hedef olmadığını bildiren **Hedef adı** alanında gösterilir.
    3.  **Hedef adı** alanının sağındaki ok düğmesini seçin.    
    4. **Elektronik raporlama adlandırılmış hedefi** sayfasında, **Ad** alanına **Ana hedef** girin.
    5. **Kaydet**'i seçin.
    6. **Dosya hedefi** hızlı sekmesinde, **Rapor** bileşeni için **E-posta** hedefini [yapılandırın](er-destination-type-email.md).
    7. **Elektronik raporlama adlandırılmış hedefi** sayfasını kapatın.
    8. **Yazdırma yönetimi kurulumu** sayfasında, **Hedef adı** alanında **Ana hedef** adlandırılmış hedefini seçin.

    ![Seçilen ER biçimi için adlandırılmış ER hedefi yapılandırma ve bunu Yazdırma yönetimi kurulum sayfasında yapılandırılmış yazdırma yönetimi kaydına atama](./media/er-named-destinations-01.gif)

    Artık **Serbest metin faturası (Excel)** biçimi için **Ana hedef** adlandırılmış ER hedefini yapılandırdınız ve bunu **Modül - alacak hesapları** \> **Belgeler** \> **Serbest metin faturası** altındaki **Orijinal** yazdırma yönetimi kaydına atadınız.

5. **Modül - alacak hesapları** \> **Hesap - US-001** \> **Serbest metin faturası**'nı genişletin, **Orijinal** kaydı seçin ve ardından şu adımları izleyin:

    1. Kaydı seçin ve basılı tutun (veya sağ tıklayın) ve ardından **Geçersiz Kıl**'ı seçin.
    2. **Hedef adı** alanının sağındaki ok düğmesini seçin.
    3. **Elektronik raporlama adlandırılmış hedefi** sayfasındaki Eylem Bölmesi'nde **Yeni**'yi seçin.
    4. **Ad** alanına, **US-001 hedefi** girin.
    5. **Dosya hedefi** hızlı sekmesinde, **Rapor** bileşeni için **Yazıcı** hedefini [yapılandırın](er-destination-type-print.md).
    6. **Elektronik raporlama adlandırılmış hedefi** sayfasını kapatın.
    7. **Yazdırma yönetimi kurulumu** sayfasında, **Hedef adı** alanında **US-001 hedefi** adlandırılmış hedefini seçin.

    ![Seçilen ER biçimi için adlandırılmış ER hedefi yapılandırma ve bunu Yazdırma yönetimi kurulum sayfasında yapılandırılmış yazdırma yönetimi kaydına atama](./media/er-named-destinations-02.gif)

    Artık **Serbest metin faturası (Excel)** biçimi için **US-001 hedefi** adlandırılmış ER hedefini yapılandırdınız ve bunu **Modül - alacak hesapları** \> **Hesap - US-001** \> **Serbest metin faturası** altındaki **Orijinal** yazdırma yönetimi kaydına atadınız.

Artık bir serbest metin faturası işlendiğinde **Serbest metin faturası (Excel)** ER biçimi çalışır ve aşağıdaki olaylardan biri gerçekleşir:

- Serbest metin faturası, US-001 haricindeki bir müşteriye aitse oluşturulan belge e-posta ile gönderilir.
- Serbest metin faturası US-001 müşterisi içinse oluşturulan belge yazdırılır.

> [!NOTE]
> Çalışma zamanında işlenen bir yazdırma yönetimi kaydı için adlandırılmış hedef tanımlanmadığında, çalışmakta olan ER biçimi için kullanılabiliyorlarsa varsayılan ER hedefleri kullanılır.

> [!IMPORTANT]
> **Elektronik raporlama hedefi** sayfasında (**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama hedefi**), en az bir adlandırılmış hedefin yapılandırıldığı bir ER biçimi seçerseniz adlandırılmış hedeflerin varlığı konusunda bilgilendirilirsiniz.
>
> ![Elektronik raporlama hedefi sayfasında seçilen ER biçimi için yapılandırılmış adlandırılmış hedeflerin varlığı hakkında bildirim](./media/er-named-destinations-03.png)
>
> Varsayılan hedefi silerseniz adlandırılmış tüm hedefler de silinir. Yazdırma yönetimi kayıtları için bu adlandırılmış hedefler seçilmişse bu adlandırılmış hedeflerin seçimi iptal edilir.

## <a name="copy-an-existing-er-destination-as-a-new-named-destination"></a>Var olan bir ER hedefini yeni bir adlandırılmış hedef olarak kopyalama

ER biçimi için varsayılan adlandırılmış ER hedefi mevcut olduğunda bu hedef yeni ER hedefleri için şablon olarak kullanılabilir. Varsayılan hedefi temel alan yeni bir ER hedefi oluşturmak için **Elektronik raporlama adlandırılmış hedefi** sayfasında **Varsayılandan kopyala**'yı seçin. Yeni hedef **Varsayılan** olarak adlandırılır. Bu adımı gerektiği kadar tekrarlayabilirsiniz.

Var olan herhangi bir adlandırılmış hedefi yeni bir adlandırılmış hedef için şablon olarak seçebilirsiniz. Seçilen adlandırılmış hedefi temel alan yeni bir adlandırılmış ER hedefi oluşturmak için **Elektronik raporlama adlandırılmış hedefi** sayfasında **Kopyala**'yı seçin. Yeni hedef, seçilen adlandırılmış hedefle aynı ada sahiptir ancak "Kopya" son eki eklenir. Bu adımı gerektiği kadar tekrarlayabilirsiniz.

## <a name="security-considerations"></a>Güvenlik ile ilgili hususlar

Yalnızca adlandırılmış ER hedeflerini ayarlama için [izniniz](../sysadmin/role-based-security.md#permissions) varsa **Yazdırma yönetimi kurulumu** sayfasında bu görevi gerçekleştirebilirsiniz. **Elektronik raporlama biçimi hedefini yapılandırma** [görevi](../sysadmin/role-based-security.md#duties), [güvenlik rollerinizden](../sysadmin/role-based-security.md#security-roles) birine atanmışsa size izin verilebilir. Daha fazla bilgi için bkz. [Güvenlik ile ilgili hususlar](electronic-reporting-destinations.md#security-considerations).

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)

[Application update 10.0.17 için elektronik raporlama çerçevesi API değişiklikleri](er-apis-app10-0-17.md)

[Application update 10.0.21 için elektronik raporlama çerçevesi API değişiklikleri](er-apis-app10-0-21.md)

[Kullanıcıların adlandırılmış ER hedeflerini yapılandırmasını ve kullanmasını sağlamak için kodu değiştirme](er-api-named-destinations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
