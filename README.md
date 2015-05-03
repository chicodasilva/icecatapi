icecatapi
=========

this bundle implements the icecat api as described here http://icecat.co.uk/en/menu/channelpartners/index.htm
by using great guzzle/guzzle webservice description, leading to a cool restful interface.

to "talk" with ebay you'll need to set following parameters in your parameters.yml

    icecat_user: [YOUR_ICECAT_USER]
    icecat_pass: [YOUR_ICECAT_PASS]
    icecat_url:  [YOUR_ICECAT_URL]
    icecat_lang: [LANGUAGE]

    Usage example:
    $icecatConnection = new IcecatConnection();
    $icecatConnection->setUser('username');
    $icecatConnection->setPassword('password');
    $icecatConnection->setUrl('http://data.icecat.biz/xml_s3/xml_server3.cgi?ean_upc={ean};lang={lang};output={output}');
    $icecatConnection->setLanguage('pt');
    $result_id = $icecatConnection->findProductInfoByEan($id);
    
    // call with product ID and Vendor
    $icecatConnection->setUrl('http://data.icecat.biz/xml_s3/xml_server3.cgi?prod_id=prod_id};vendor={vendor};lang={lang};output={output}');
    $result_ProdID = $icecatConnection->findProductInfoByVendorProdID('Samsung','GT-I9515ZSAATO');
