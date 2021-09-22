---
title: Uygulama bağlantısı ayarlanırken sertifika yolu hatası
description: Warehouse Management uygulamasında "Sertifika yolu için güven çıpası bulunamadı" hatası görüntüleniyorsa sorunu çözmek veya geçici bir çözüm bulmak için bu sayfayı kullanın.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477851"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Uygulama bağlantısı ayarlanırken sertifika yolu için güven çıpası bulunamadı

## <a name="symptoms"></a>Belirtiler

Supply Chain Management'a bağlanmayı denerken Warehouse Management uygulamasında aşağıdaki hata iletisini görebilirsiniz:

> java.security.cert.certPathValidatorException: Sertifika yolu için güven çıpası bulunamadı.

Bu sorun, aşağıdaki özelliklerin bulunduğu cihazları etkileyebilir:

- **İşletim sistemi sürümü**: Android 4.4.x (örneğin, Zebra TC55). Bu, en son Android sürümlerinde karşılaşılan bir sorun değildir.
- **Supply Chain Management konumu**: Bulut
- **Bağlantı modu**: İstemci gizli anahtarı veya sertifikası

## <a name="possible-cause"></a>Olası neden

Microsoft, Supply Chain Management tarafından kullanılan sunucu SSL sertifikalarını güncelleştirmiş olabilir. Sonuç olarak, kök sertifika ve/veya ara sertifikalardan biri değişmiş olabilir, bu nedenle yeni sertifika mobil cihaz için güvenilen sistem sertifikaları listesinde değildir. Android'in daha yeni sürümleri, güvenilen sertifika listelerini otomatik olarak güncelleştirir ancak Android 4.4.x sürümü bunu yapmaz.

## <a name="resolution"></a>Çözüm

Bu sorunu çözmek için aşağıdakilerden birini yapın:

- İlgili tüm cihazları güncelleştirmek için sonraki bölümde açıklanan geçici çözümü kullanın.
- Sistem güvenilen sertifika yetkilisi (CA) sertifikalarının güncelleştirmesini almak için Zebra veya Google ile iletişime *geçilebilir*. Ancak bu durum tarafımızdan onaylanmamıştır.
- Mümkünse, eski cihazları Android'in (güvenilen CA sertifikalarının otomatik olarak güncelleştirildiği) daha yeni bir sürümünü çalıştıran cihazlarla değiştirebilirsiniz.

### <a name="workaround"></a>Geçici çözüm

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>1. Adım: Yeni kök sertifikayı Supply Chain Management uygulamasından dışarı aktarın

Aşağıdakileri gerçekleştirerek internet tarayıcınızla yeni kök sertifikayı el ile indirin:

1. Dynamics Supply Chain Management uygulamasında oturum açıp ön sayfayı açın.

1. **Konum güvenli** iletişim kutusunu açmak için tarayıcınızın adres çubuğunda kilit simgesini seçin.
1. İletişim kutusunda, bu sertifikanın **Sertifika** penceresini açmak için **Sertifika (geçerli)** seçeneğini belirleyin.
1. **Sertifika** penceresinin **Sertifika yolu** sekmesini açın.
1. Hiyerarşide gösterilen üst sertifikayı seçin. (Bu, kök sertifikadır).
1. **Sertifika** penceresinin **Ayrıntılar** sekmesini açın.
1. **Ayrıntılar** sekmesinin altındaki **Dosyaya kopyala** düğmesini seçin.
1. **Sertifika dışarı aktarma sihirbazı** açılır. Devam etmek için **İleri**'yi seçin.
1. **Dışarı aktarma dosya biçimi** sayfası açılır. **DER ile kodlanmış ikili X.509 (.CER)** öğesini seçin. Ardından devam etmek için **İleri**'yi seçin.
1. Açılan **Dışarı aktarılacak dosyalar** sayfasında dosya adını ve konumunu belirtin. Ardından devam etmek için **İleri**'yi seçin.
1. Dışarı aktarma işleminizin sonucunu gösteren **Sertifika dışarı aktarma sihirbazı tamamlanıyor** sayfası açılır. **Bitir**'i seçin.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>2. Adım: İndirilen sertifikayı etkilenen cihazlara yükleyin

Aşağıdakileri yaparak indirilen sertifikayı yükleyin:

1. Önceki adımda indirdiğiniz sertifikayı güncelleştirmek istediğiniz cihaza aktarın. Örneğin, dosyayı cihazınızda kullanılabilir hale getirmek için bir SD kart veya ağ bağlantısı kullanabilirsiniz.
1. Cihazınızın güvenlik ayarlarını açın ve bir dosyadan sertifika yüklemek üzere menü seçeneğini belirleyin. (Bu işlemin doğru adımları cihaza ve işletim sistemi sürümüne göre değişiklik gösterir.)
1. Yeni sertifika, artık güvenilen sertifikalar için **Kullanıcı** sekmesinde görüntülenmelidir.
1. Etkilenen her cihaz için bu yordamı tekrarlayın.
