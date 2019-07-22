---
title: E-posta ayarlarını Microsoft Dynamics 365 for Talent - Attract'ta Yapılandır
description: Bu konu, Microsoft Dynamics 365 For Talent - Attract tarafından gönderilen e-posta ayarlarının nasıl yapılandırılacağını açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 360937b807ea149edb2f16ad6799d74791d599b5
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729807"
---
# <a name="configure-email-settings-in-microsoft-dynamics-365-for-talent---attract"></a>E-posta ayarlarını Microsoft Dynamics 365 for Talent - Attract'ta Yapılandır
[!include[banner](../includes/banner.md)]

Markanız güven oluşturur ve pozisyonlarınıza başvurmadan önce adaylarla bir ilişki kurmanıza yardımcı olur. Olumlu marka algısı en yeteneklilerin ilgisini çeker ve mevcut çalışanların da bağlılığını kuvvetlendirir. Microsoft Dynamics 365 for Talent: Attract şirketinizin markasını yansıtması için e-postaları yapılandırmanızı sağlar. Bu nedenle, iş adaylarıyla başvuru süreci boyunca tutarlı bir deneyim sağlayabilirsiniz.

Attract aşağıdaki eylemleri gerçekleştirmenizi sağlar:

- E-posta ayarlarını şirketinizin Microsoft Exchange e-posta hizmeti hesabı kullanılacak şekilde yapılandırın. Böylece adaylar, e-postaların şirkettinizden geldiğini bilir. Örneğin ayarlarınızı adaylarınızın e-postalarınızı `contoso@microsoft.com` yerine `recruiting@contoso.com` adresinden almalarını sağlayacak şekilde yapılandırabilirsiniz.
- E-posta şablonları için genel bir üstbilgi ve altbilgi ayarlayarak tüm e-posta iletişimleriniz için tutarlı bir marka oluşturun. 

> [!NOTE]
> Attract'i e-posta göndermek amacıyla şirketinizin e-posta hizmeti hesabını kullanacak şekilde yapılandırmak için Kapsamlı işe alma eklentisi gerekir.

## <a name="connect-an-email-service-account"></a>E-posta hizmet hesabına bağlanın

Şirketinizin e-posta hizmeti hesabına bağlanarak iş adaylarınız için markalı bir e-posta deneyimi oluşturabilirsiniz. Şirket hesabınızı bağlamazsanız Attract, varsayılan Microsoft markalı e-posta hizmeti hesabını kullanır.

1. **Ayarlar** düğmesini (sayfanın sağ üst köşesindki çark simgesi) seçin ve sonra **Yönetici merkezini** seçin.
2. **E-posta ayarları** sekmesinde, **E-posta hizmeti hesapları** altında **Şirket hesabı bağla**'yı seçin.

    ![Şirketinizin e-posta hizmeti hesabına Attract'te bağlama](./media/attract-admin-email-service-accounts.png)

    Paylaşılan bir e-posta hesabı oluşturma hakkında daha fazla bilgi için [Paylaşılan e-posta hesabı Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes)'deki paylaşılan posta kutularına bakın.

3. Microsoft oturum açma penceresinde, şirket kimlik bilgilerinizi kullanarak oturum açın.
4. Henüz bir e-posta hizmeti hesabı ayarlamadıysanız veya yeni bir hesap eklemek istiyorsanız **Yeni hizmet hesabı ekle**'yi seçin ve sonra e-posta bilgilerinizi girin. Kullanmak istediğiniz e-posta hizmeti hesabını zaten ayarladıysanız onu seçin.

E-posta hizmeti hesabınız başarıyla yapılandırıldığında, bunu **E-posta hizmeti hesapları altında** görebilirsiniz.

## <a name="disconnect-an-email-service-account"></a>E-posta hizmet hesabıyla bağlantıyı kesin

E-posta iletişiminde şirketinizin etki alanını, Attract kullanarak durdurmak istiyorsanız bir e-posta hizmeti hesabının bağlantısını kesebilirsiniz.

1. **Ayarlar** düğmesini (sayfanın sağ üst köşesindki çark simgesi) seçin ve sonra **Yönetici merkezini** seçin.
2. **E-posta ayarları** sekmesinde, **E-posta hizmeti hesapları** altında, kesmek istediğiniz e-posta hizmeti hesabının yanındaki **Daha fazla** düğmesini (üç dikey nokta) seçin.
3. **E-posta hesabı bağlantısını kes**'i seçin.

    ![Şirketinizin e-posta hizmeti hesabının bağlantısını kesme](./media/attract-admin-disconnect-email-account.png)

4. İşlemi onaylamanız istendiğinde, **Bağlantıyı kes**'i seçin.

    ![Şirketinizin e-posta hizmeti hesabının bağlantısının kesilmesini onaylama](./media/attract-admin-email-confirm-disconnect.png)

Farklı bir e-posta hizmeti hesabı bağlamazsanız Attract'tan atılan e-postalarda varsayılan olarak Microsoft markalı e-posta hizmeti hesabı kullanılır.

## <a name="configure-email-template-settings"></a>E-posta şablonu ayarlarını yapılandırma

Şirketinizin logosunu ve diğer bilgileri e-postalarınızın markalı başlığı olması için karşıdan yükleyebilirsiniz. Ayrıca e-posta altbilgilerindeki Gizlilik ilkenize ve kullanım koşullarına da bağlantı sağlayabilirsiniz.

> [!NOTE]
> Ülkenizde, bölgenizde ve e-posta alıcısının ülkesinde ve bölgesinde yürürlükte olan tüm yasalara uymanız gerekir. Bu yasalar istenmeyen posta önleme düzenlemeleri içerir.

1. **Ayarlar** düğmesini (sayfanın sağ üst köşesindki çark simgesi) seçin ve sonra **Yönetici merkezini** seçin.
2. **E-posta ayarları** sekmesinde, **E-posta şablonu ayarları** altında, e-posta üstbilgileriniz olarak kullanmak istediğiniz görüntüyü görüntü kutusuna sürükleyin veya dosyaya gözatmak için görüntü kutusuna tıklayın. Varolan bir görüntüyü değiştirmek için önce görüntünün yanındaki **Kaldır**'ı seçmelisiniz. Görüntü bir JPEG, JPG, PNG veya SVG dosyası olmalıdır. Görüntüler için önerilen boyut 25-800 piksel genişliğinde ve 25 ila 150 piksel yüksekliğindedir. Başlık için maksimum dosya boyutu 1 megabayttır (MB).

    ![Şirketinizin e-posta üstbilgisine resim ekleme](./media/attract-admin-email-header.png)

3. **İletişim için Gizlilik politikanızın** altında şirketinizin gizlilik ilkesine bir bağlantı sağlayın. **İletişim için Hüküm ve Koşullarınızın** altında şirketinizin kullanım koşullarına bir bağlantı sağlayın.

    ![Şirketinizin gizlilik politikasına ve e-posta alt bilgisi ile ilgili kullanım koşullarına bağlantılar ekleme](./media/attract-admin-email-footer.png)

4. E-posta şablon ayarlarınızı kaydetmek için **Kaydet**'i seçin.
