---
title: Müşteri ön ödemeleri
description: Bu makalede, müşteri ön ödemelerinin (müşteri depozitoları olarak da bilinir) nasıl ayarlanacağı ve işleneceği açıklanmaktadır.
author: twheeloc
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88773067c472471fb75167712268d1076c1738a5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861574"
---
# <a name="customer-prepayments"></a>Müşteri ön ödemeleri

[!include [banner](../includes/banner.md)]

Müşteri ön ödemeleri, bir müşteriden ödeme aldığınızda ancak ödemeyle ilgili olarak kapatılabilecek bir fatura olmadığında kullanılır. Bu ödeme türleri, müşteri mevduatları olarak da adlandırılır.

Müşteri ön ödemelerinin ayarlanması ve bunlarla çalışmak, aşağıdaki temel adımlardan oluşur.

1. Ön ödemeler için müşteri deftere nakil profili oluşturun.
2. **Ön ödeme günlüğü fişi için nakil profili** parametresini ayarlayın.
3. Bir müşteri ödeme günlüğü oluşturun ve her satırda **Ön ödeme günlüğü fişi** onay kutusunu seçin.
4. Müşteri ödeme günlüğünü naklet.
5. Bir fatura oluşturulduktan sonra, **Açık hareketleri kapat** sayfasını kullanarak bu ön ödemeyi kapatın.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Ön ödemeler için müşteri deftere nakil profili oluşturma

Genellikle, mal veya servisler teslim edilmeden veya sisteminizde bir fatura var olmadan önce müşteriden ön ödeme veya mevduat kabul ettiğinizde, hesap planında nakiti varlık olarak değil borç olarak kaydetmeniz gerekir. Ancak, bu tutarların genel muhasebenizdeki kayıt gereksinimleri ülkenize veya bölgenize göre farklılık gösterebilir. Bu nedenle, ilgili tüm yerel düzenlemeler hakkında muhasebecinize başvurun.

Genel olarak, ön ödemeler için kullanılabilecek bir deftere nakil profili oluşturma işlemi, diğer deftere nakil profillerini oluşturma işlemiyle aynıdır. Temel fark, **Özet hesap** alanında seçtiğiniz ana hesaptır. Daha fazla bilgi için [Müşteri deftere nakil profilleri](customer-posting-profiles.md) konusuna bakın.

## <a name="define-parameters-for-customer-prepayments"></a>Müşteri ön ödemeleri için parametreleri tanımlama

Müşteri ön ödemeleri için sistemi yapılandırırken dikkate almanız gereken iki ana alacak hesabı parametresi vardır. Parametreleri yapılandırmak için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.
2. İsteğe bağlı: **Genel muhasebe ve satış vergisi** sekmesinde, **Ödeme** hızlı sekmesinde, **Ön ödeme günlüğü fişinde satış vergisi** seçeneğini **Evet** olarak ayarlayın.
3. **Ön ödeme günlüğü fişiyle nakil profili** alanında, müşteri ön ödemeleri deftere nakledildiğinde kullanılacak müşteri nakil profilini seçin.
4. Sayfayı kapatın.

## <a name="create-customer-prepayment-vouchers"></a>Müşteri ön ödeme fişleri oluşturma

Müşteri ödeme günlüğünü oluşturduğunuzda, her ön ödeme için, **Müşteri ödeme günlüğü** sayfasında **Ön ödeme günlüğü fişi** seçeneğini **Evet** olarak ayarlamalısınız. Müşteri ön ödemesi oluşturmak için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Ödemeler \> Müşteri ödeme günlüğü** seçeneğine gidin.
2. Bir günlük oluşturmak için **Yeni**'yi seçin.
3. **Ad** alanında, kullanılacak günlük adını seçin.

    > [!IMPORTANT]
    > Önceki prosedürde **Ön ödeme günlüğü fişinde satış vergisi** seçeneğini **Evet** olarak ayarladıysanız, **Tutara satış vergisi dahildir** parametresinin seçili olduğu bir günlük adı seçmeniz gerekir. 

4. İsteğe bağlı: **Açıklama** alanına ayrıntılı bir açıklama girin.
5. **Satırlar**'ı seçin.
6. Boş bir satır yoksa, bir satır oluşturmak için **Yeni**'yi seçin.
7. **Tarih** alanına, ön ödemenin deftere nakledilmesi gereken tarihi girin.
8. **Hesap** alanında, ön ödemenin müşterisini seçin.
9. İsteğe bağlı: **Açıklama** alanına hareketin ayrıntılı bir açıklamasını girin.
10. **Alacak** alanına, ön ödeme tutarını girin.
11. **Mahsup hesabı** alanında, ödemenin mahsup edileceği hesabı seçin. Örneğin, ödemenin nakledileceği banka veya ana hesabı seçin.
12. **Ödeme yöntemi** alanında, müşterinin ödeme yöntemini seçin.
13. **Ödeme** sekmesinde, **Ön ödeme günlüğü fişi** seçeneğini **Evet** olarak ayarlayın.
14. Deftere nakledilmesi gereken her ek ön ödeme için 7 ile 13 arasındaki adımları yineleyin.
15. Günlüğü tamamlamak için **Deftere naklet**'i seçin.

## <a name="settle-prepayments-with-invoices"></a>Ön ödemeleri faturalarla kapatma

Tam olarak kapatılmayan ödemeleri kolayca bulmak ve kapatmak için **Müşteri ödemeleri** çalışma alanını kullanabilirsiniz.

1. **Giriş** panosunda, **Müşteri ödemeleri** kutucuğunu seçin.
2. **Müşteri hareketleri** bölümünde, **Ödemeler kapatılmadı** sekmesinde, kapatılacak ödemeyi arayıp seçin.
3. **Hareketleri kapat** öğesini seçin.
4. Fatura ve kapatılacak ödeme için **İşaretle** onay kutusunu seçin.
5. **Naklet**'i seçin.

Açık hareketlerin nasıl kapatılacağı hakkında daha fazla bilgi için bkz. [Kapatmaya genel bakış](/dynamics365/finance/cash-bank-management/settlement-overview).
