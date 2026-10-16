<!DOCTYPE html>
<html>
<head>
<title>BS3G Live - $307 to $3000</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>body{background:#0a0a0a;color:#fff;font-family:sans-serif;text-align:center;padding:20px}.price{font-size:42px;color:#ffd700;font-weight:bold} iframe{width:100%;height:600px;border:none;border-radius:16px;margin-top:20px}</style>
</head>
<body>
<h1>BS3G - Bo Source 3G</h1>
<div class="price" id="livePrice">$376.96 LIVE</div>
<p>Contract: 0x6db31Fd7a8868bD9ed24371259b7677640F0e6EA</p>
<p>6.00M Total Supply | 81 Holders</p>

<!-- LIVE CHART -->
<iframe src="https://dexscreener.com/bsc/0x6db31Fd7a8868bD9ed24371259b7677640F0e6EA?embed=1&theme=dark"></iframe>

<script>
// Auto refresh price from DexScreener API
async function getPrice(){
 try{
  const res = await fetch('https://api.dexscreener.com/latest/dex/tokens/0x6db31Fd7a8868bD9ed24371259b7677640F0e6EA');
  const data = await res.json();
  if(data.pairs && data.pairs[0]){
    document.getElementById('livePrice').innerText = '$' + data.pairs[0].fdv + ' FDV LIVE';
  }
 }catch(e){}
}
setInterval(getPrice, 5000);
getPrice();
</script>
</body>
</html>