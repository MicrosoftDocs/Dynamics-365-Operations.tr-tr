---
title: E-posta kanalı yapılandırma
description: Bu makalede, e-posta kanalının elektronik faturaları alacak şekilde nasıl yapılandırılacağı açıklanmaktadır.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9227b032ffe896ad6a67962e5047fd797a883ae1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902399"
---
# <a name="configure-an-email-channel"></a>E-posta kanalı yapılandırma

[!include [banner](../includes/banner.md)]

Oluşturduğunuz Elektronik faturalama özelliği, e-posta ile alınan ekli dosyalardan elektronik satıcı faturalarını içe aktarıyorsa bir e-posta hesabı kanalı yapılandırmanız gerekir.

1. Regulatory Configuration Services'te (RCS), oluşturduğunuz Elektronik faturalama özelliğini seçin. **Taslak** durumunda olan sürümü seçtiğinizden emin olun.
2. **Kurulumlar** sekmesinde **Ekle**'yi seçin.
3. **Özellik kurulumu oluştur** açılan iletişim kutusunda, **Yeni** alan grubunda, **Özel kurulum** seçeneğini belirleyin.
4. **Kurulum türü** alan grubunda, **Veri kanalı** seçeneğini belirleyin.
5. **Veri kanalı seç** alanına, **Gelen e-posta** girin.
6. **Oluştur**'u seçin.
7. Oluşturduğunuz satırı seçin ve sonra **Düzenle**'yi seçin.
8. **Veri kanalı** sekmesinde, **Parametreler** bölümünde aşağıdaki gerekli alanları ayarlayın.

    | Alan                | Açıklama |
    |----------------------|-------------|
    | Veri kanalı         | Veri kanalını tanımlamak için benzersiz bir ad girin. Ad en fazla 10 karakter uzunluğunda olabilir. İletişim işlemi sırasında, uygulanabilirlik kurallarında ve bağlı uygulamalarda başvurulacak. |
    | Sunucu adresi       | E-posta hesabı sağlayıcısı alanına sunucu adresini girin. Örneğin, `https://outlook.live.com` sağlayıcısı için sunucu adresi imap-mail.outlook.com'dur. |
    | Sunucu bağlantı noktası          | E-posta hesabı sağlayıcısının kullandığı bağlantı noktası numarasını girin. Örneğin, `https://outlook.live.com` sağlayıcısı için sunucu bağlantı noktası 993'tür. |
    | Kullanıcı adı gizli anahtarı     | E-posta kullanıcı hesabının kimliğini içeren Microsoft Azure Key Vault'un adını girin. Bu gizli dizi, Key Vault'ta oluşturulmalı ve hizmet ortamınızda kurulmalıdır. |
    | Kullanıcı parolası gizli anahtarı | E-posta kullanıcı hesabının parolasını içeren Key Vault gizli dizisi adını girin. |
    | Zaman aşımı              | Sistemin yanıt beklemesi için bekleyeceği, milisaniye (ms) cinsinden en fazla süre sınırı. Varsayılan değer 10.000 ms'dir (10 saniye). |
    | Ana klasör          | E-posta alma kaynağını veya hizmetin e-postaları işlemesi gereken klasörü belirtin. |
    | Arşiv klasörü       | İşlenen e-postaların depolanacağı klasörü belirtin. Bu klasörü belirlemezseniz, sistem otomatik olarak bunu oluşturur. |
    | Hata klasörü         | Sistemin işlem başarısız olduğunda e-postaları taşımak için kullanacağı klasörü belirtin. Bu klasörü belirlemezseniz, sistem otomatik olarak bunu oluşturur. |
    | Maksimum ileti boyutu     | İşlenen tek bir iletinin en büyük boyutunu bayt olarak girin. Varsayılan değer 20.000.000 bayttır. |
    | Maksimum ileti sayısı   | Tek bir eylem için işlenecek maksimum ileti sayısını girin. İletilerin sayısını sınırlandırmak istemiyorsanız, değeri **0** (sıfır) olarak ayarlayın. |
    | Kimden filtresi          | Gönderen adresine göre filtrelemek için bir dize girin. Yalnızca gönderen adresinin filtreyle eşleştiği e-postalar işlenir. Bu alan isteğe bağlıdır. Birden fazla gönderen adresi belirtmek için ayırıcı olarak noktalı virgül (;) kullanın. |
    | Konu filtresi       | Konuya göre filtrelemek için bir dize girin. Yalnızca konunun filtreyle eşleştiği e-postalar işlenir. Bu alan isteğe bağlıdır. **\*smth\*.ext** gibi basit maskeler desteklenir, her bir yıldız işareti (\*) sıfırı veya herhangi bir karakterin birden fazla tekrarlanmasını temsil eder. |
    | Veri filtresi          | İşlenen iletilerin gün cinsinden maksimum yaşını tanımlamak için bir tarih belirtin. Bu alan isteğe bağlıdır. Varsayılan değer 30 gündür. |
    | İşleme modu      | <p>Bir e-postadaki tüm eklerin birlikte işlenebilir olup olmayacağını veya her ekin ayrı olarak işlenip işlenmeyeceğini belirtmek için aşağıdaki seçeneklerden birini belirleyin:</p><ul><li><b>Eke göre</b> – E-postadaki her ek için yeni bir elektronik belge oluşturulur. Örneğin, bir e-posta e-fatura verilerini içeren birkaç dosya içeriyorsa, her bir dosya sistemde yeni bir e-fatura olarak kabul edilir.</li><li><b>E-postaya göre</b> – Bir ek, temel ek olarak kabul edilir ve sistemde bir elektronik fatura oluşturulur. Diğer ekler, destek dosyaları olarak kullanılabilir.</li></ul> |

9. **Ekler filtresi** bölümünde, dosya filtreleme bilgilerini ekleyin. Yalnızca tanımlanan filtreye uyan ekler işlenecektir. Örneğin, **\*.xml**, .xml dosya adı uzantısına sahip ekleri filtreler. Ekin adı, kurulum sırasında Dynamics 365 Finance veya Dynamics 365 Supply Chain Management'ta kullanılır.

    - Önceki adımda **İşleme modu** alanını **E-postaya göre** olarak ayarlarsanız, buraya birden fazla filtre ekleyebilirsiniz. Ad, belirli belgeyi tanımlar.
    - **İşlem modu** alanını **Eke göre** olarak ayarlarsanız, yalnızca bir filtre ekleyebilirsiniz.

10. **Uygulanabilirlik kuralları** sekmesinde, ölçütleri gerektiği şekilde inceleyip güncelleştirin. **Kanal** alanının değeri 8. adımdaki **Veri kanalı** alanına girdiğiniz değere eşit olmalıdır.
11. **Kaydet**'i seçip sayfayı kapatın.
