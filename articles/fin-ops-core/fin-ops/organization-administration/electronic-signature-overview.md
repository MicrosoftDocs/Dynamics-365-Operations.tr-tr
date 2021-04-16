---
title: Elektronik imzalara genel bakış
description: Bu makale, elektronik imzalara genel bakış sağlar ve nasıl kullanılabileceklerini açıklar.
author: maertenm
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SIGParameters, SIGProcSetup, SIGReasonCode
audience: Application User
ms.reviewer: sericks
ms.custom: 13611
ms.assetid: 98dc6b79-1895-45d8-9dd1-2c8a351b58af
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 547ab10dabb6bb3f8ea41d0f80db227fc24411a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747723"
---
# <a name="electronic-signatures-overview"></a>Elektronik imzalara genel bakış

[!include [banner](../includes/banner.md)]

Bu makale, elektronik imzalara genel bakış sağlar ve nasıl kullanılabileceklerini açıklar.

## <a name="what-is-an-electronic-signature"></a>Elektronik imza nedir?

Elektronik imza bir hesaplama işlemi başlatmak veya onaylamak üzere olan kişinin kimliğini doğrular. Bazı sektörlerde, elektronik imza yasal açıdan elle atılmış imza kadar bağlayıcı olmaktadır.

Elektronik imzalar ilaç, yiyecek ile içecek ve havacılık ve uzay ile savunma sanayileri gibi birtakım kontrol altındaki sektörlerle ilgili yönetmeliklere uyumluluk gereklilikleridir. Aynı zamanda ABD'de İlaç ve Gıda Dairesi (FDA) tarafından yayınlanmış 21 CFR Bölüm 11'deki yönetmeliklere uygunluk açısından da gereklidir.

> [!NOTE]
> Elektronik imza kendi başına dijital imzayla aynı değildir. Dijital imza başka güvenlik önlemleri de sağlarken, elektronik imza sadece el yazısı imzanın yerini tutar. Dijital imza verilere başka bir kullanıcı veya işlem tarafından müdahale edilip edilmediğini belirlemeye yardımcı olabilir. Dijital imzalar da doğrulanabilir ve bu doğrulama, verilerin imzalanmasında kullanılan sertifikanın sahibi tarafından reddedilemez. Aşağıda açıklandığı gibi, elektronik imzaların yerleşik dijital imza işlevleri vardır.

## <a name="electronic-signatures"></a>Elektronik imzalar

Önemli iş süreçleri için elektronik imza kullanabilirsiniz. Bazı işlemler yerleşik elektronik imza özelliklerine sahiptir. Ayrıca herhangi bir veritabanı tablosu ve alanı için özel imza gereklilikleri de oluşturabilirsiniz.

Elektronik imzaların yerleşik dijital imza işlevleri vardır. Belge imzalayan her bir kullanıcı geçerli bir kriptografik sertifika edinmelidir. Bir belge imzalandığında, o sertifika ile ilişkilendirilmiş olan özel anahtar doğrulanır. Elektronik imza bilgileri denetim kılavuzu sağlamak için bir günlüğe kaydedilir. Elektronik imzaları ayarlamak için bkz. [Elektronik imza ayarlama](tasks/set-up-electronic-signatures.md).

## <a name="users-who-require-access-to-electronic-signatures"></a>Elektronik imza erişimi gerektiren kullanıcılar

Elektronik imzalara güvenlik erişimine genellikle üç tür kullanıcının ihtiyacı olur: elektronik imza yöneticileri, imzalayanlar ve elektronik imza denetçileri.

### <a name="electronic-signature-administrator"></a>Elektronik imza yöneticisi

Elektronik imza yöneticisi, imza gerekliliklerini, genel parametreleri ve onaylayanları ayarlar ve imza doğrulanamadığında uyarılar alır. Varsayılan olarak, **Bilgi teknolojisi yöneticisi** güvenlik rolüne ait olan bir kullanıcı, elektronik imza yönetimi iznine sahiptir.

### <a name="signer"></a>İmzalayan

İmzalayan, imza gereken belge ve işlemler için elektronik imza sağlar. Varsayılan olarak, **Sistem kullanıcısı** güvenlik rolüne ait bir kullanıcı belgeleri elektronik olarak imzalama iznine sahiptir.

> [!NOTE]
> İmzalayan, imzalanan belge veya işlemle ilgili verilere erişim sağlanmadan önce ek izinlere gereksinim duyabilir. Verilerde değişiklik yapan ve ardından bu değişiklikler için imzası gereken bir kullanıcının verileri değiştirme izni olmalıdır. Başka bir kullanıcı adına imzalayan kullanıcının verilere erişmesi gerekmeyebilir. Bu tür bir kullanıcıya örnek olarak çalışanın değişikliklerini imzalayan gözetmen verilebilir.

### <a name="electronic-signature-auditor"></a>Elektronik imza denetçisi

Elektronik imza denetçisi veritabanı günlüğünü ve veritabanı günlüğünde bulunan imza inceleme günlüğünü gözden geçirir. Varsayılan olarak, **Bilgi teknolojisi yöneticisi** güvenlik rolüne ait olan bir kullanıcı, elektronik imza denetimi iznine sahiptir.

**Bilgi teknolojisi yöneticisi** dışında bir rol kullanıyorsanız, role aşağıdaki ayrıcalıkların atandığından emin olun:

- Elektronik imza hatalarını görüntüle
- Veritabanı günlüğünü görüntüle

## <a name="signing-documents-electronically"></a>Belgeleri elektronik olarak imzalama

### <a name="get-a-certificate"></a>Sertifika alma

Belgeleri elektronik olarak imzalamadan önce, bir sertifika istemeniz gerekir.

> [!NOTE]
> Microsoft SQL Server özellikleri sertifika oluşturmak ve elektronik imzalamaya olanak vermek için kullanılır. Başka sertifika veya ortak anahtar altyapısı (PKI) gerekmez.

Bir sertifika istediğinizde, sizin için bir ortak anahtar ve bir özel anahtar oluşturulur. Özel anahtar yalnızca sizin bildiğiniz bir parola kullanılarak şifrelenir. Bir belgeyi elektronik olarak imzaladığınız zaman, parolanızı girdiğinizde kimliğiniz doğrulanır.

Sertifika istemek için, **Seçenekler** sayfasında **Hesaplar** sekmesinde **Sertifika al** öğesine tıklayın.

İmzalamak için kullanacağınız parolayı girmeli ve onaylamalısınız. Parola, özel anahtarınızı korumak ve sertifika kullanımını yetkilendirmek için kullanılır. Bu parola, veritabanında saklanmaz ve yönetici de dahil olmak üzere başka kimse tarafından kullanılamaz.

Sertifikanızla bağlantılı parolayı unutursanız, sertifikanın sıfırlanması gerekir. Sertifikayı sıfırlarsanız, önceki sertifikayı kullanarak imzaladığınız belgeleri etkilemezsiniz. Sertifikayı sıfırlamak için **Seçenekler** sayfasında **Sertifikayı sıfırla** öğesine tıklayın.

### <a name="sign-a-document-electronically"></a>Belgeyi elektronik olarak imzalama

Elektronik imza gerektiren bir değişiklik yaptığınızda **Belgeyi imzala** sayfası görüntülenir.

1. Belgede yapılan değişiklikleri gözden geçirmek için **Belgeyi imzala** sayfasında **Belge** sekmesine tıklayın.
2. **İmza** sekmesinde, bir neden kodu seçin.
3. Açıklama gerekirse bir açıklama girin.
4. Kullanıcı kimliğiniz **İmzalayan** alanında görünmezse, listeden seçin.
5. Bu bilgi gerekiyorsa, konumunuzu girin.
6. **Tamam** düğmesine tıklayın.

### <a name="sign-for-another-users-changes"></a>Başka bir kullanıcının değişiklikleri için imzalama

Bazen bir kullanıcının, başka bir kullanıcının değişiklikleri için imza atmasını isteyebilirsiniz. Örneğin, bir çalışanın ürün reçetelerinde yaptığı değişiklikler için bir gözetmenin imzalaması gerekebilir. Bir kullanıcıyı başka bir kullanıcı için imzalayan olarak belirtmek için bu yordamı kullanın.

> [!NOTE]
> Bir kullanıcı başka bir kullanıcının değişikliği için imzaladığında, imzanın, değişikliği yapan kullanıcının iş istasyonundan girilmesi gerekir. İmza girilene kadar kullanıcı değişikliği kaydedemez.

Onaylayanları belirlemek için aşağıdaki adımları izleyin.

1. **Seçenekler** sayfasında **Hesaplar** sekmesinde **Onaylayanı belirle** öğesine tıklayın.
2. **Onaylayan kullanıcının kimliği** alanında, başka bir kullanıcının değişikliklerini imzalaması gereken kullanıcı kimliğini seçin.
3. **Kullanıcı kimliği için imza yetkisi** alanında, değişiklikleri imzalanacak kullanıcının kimliğini seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]