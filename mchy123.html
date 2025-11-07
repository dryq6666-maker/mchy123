<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>猛插何一 - MCHY 预售空投 (1 BNB = 10M MCHY)</title>
    <script src="https://cdn.ethers.io/lib/ethers-5.7.umd.min.js" type="application/javascript"></script>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; background: linear-gradient(to bottom, #ff69b4, #ffd700); color: #333; }
        #game-area { margin: 20px; padding: 20px; border: 2px solid #ff1493; border-radius: 15px; box-shadow: 0 4px 8px rgba(255,20,147,0.3); }
        button { background: #ff1493; color: white; padding: 12px 24px; font-size: 18px; border: none; border-radius: 8px; cursor: pointer; margin: 5px; }
        button:hover { background: #c71585; transform: scale(1.05); }
        button:disabled { background: #ccc; cursor: not-allowed; transform: none; }
        #animation { font-size: 60px; margin: 15px; transition: all 0.5s; }
        .warning { color: #ff4500; font-weight: bold; background: #fff3cd; padding: 10px; border-radius: 5px; margin: 10px; }
        #status { font-size: 16px; margin: 10px; padding: 8px; border-radius: 5px; }
        .success { background: #d4edda; color: #155724; }
        .error { background: #f8d7da; color: #721c24; }
        .mchy { color: #ffd700; font-weight: bold; font-size: 20px; }
    </style>
</head>
<body>
    <h1>🔥 猛插何一 - MCHY 预售空投 🔥<br><small>1 BNB = 10,000,000 MCHY | 0.01 BNB = 100,000 MCHY</small></h1>
    <p class="warning">⚠️ 预售中！每“猛插” = 转 0.01 BNB 到 0xa66c4c7e89b31496717aa1eb3b27e250c0e8d328 → 赚 100k MCHY 空投份额。燃气自理，测试网练手。空投待定，非投资！</p>
    
    <div id="game-area">
        <p>当前猛插次数: <span id="count">0</span></p>
        <p>你的 BNB 余额: <span id="balance">未连接</span></p>
        <p class="mchy">投影空投 MCHY: <span id="mchy">0</span></p>
        <p>总贡献 BNB: <span id="totalBNB">0</span></p>
        <button id="connectBtn" onclick="connectWallet()">1️⃣ 连接钱包 (BSC)</button>
        <button id="mengchaBtn" onclick="mengcha()" style="display:none;">2️⃣ 猛插何一！（+100k MCHY）</button>
        <div id="animation">😏 预售启动，等你贡献</div>
        <div id="status">连接钱包，切换 BSC 主网 (Chain ID: 56) 开始预售...</div>
    </div>

    <script>
        let provider, signer, count = 0, mchy = 0, totalBNB = 0, userAddress;
        const RECIPIENT = '0xa66c4c7e89b31496717aa1eb3b27e250c0e8d328';
        const AMOUNT = ethers.utils.parseEther('0.01');
        const MCHY_PER_BNB = 10000000; // 1 BNB = 10M MCHY
        const BSC_CHAIN_ID = '0x38'; // 主网 56

        async function connectWallet() {
            if (typeof window.ethereum === 'undefined') {
                alert('🚫 请安装 MetaMask 或兼容钱包！');
                return;
            }

            try {
                provider = new ethers.providers.Web3Provider(window.ethereum);
                const accounts = await provider.send("eth_requestAccounts", []);
                signer = provider.getSigner();
                userAddress = await signer.getAddress();

                // 链切换/添加
                const network = await provider.getNetwork();
                if (network.chainId !== parseInt(BSC_CHAIN_ID, 16)) {
                    try {
                        await window.ethereum.request({
                            method: 'wallet_switchEthereumChain',
                            params: [{ chainId: BSC_CHAIN_ID }],
                        });
                    } catch (switchError) {
                        if (switchError.code === 4902) {
                            await window.ethereum.request({
                                method: 'wallet_addEthereumChain',
                                params: [{
                                    chainId: BSC_CHAIN_ID,
                                    chainName: 'Binance Smart Chain Mainnet',
                                    rpcUrls: ['https://bsc-dataseed1.binance.org/'],
                                    nativeCurrency: { name: 'BNB', symbol: 'BNB', decimals: 18 },
                                    blockExplorerUrls: ['https://bscscan.com']
                                }],
                            });
                        } else {
                            throw switchError;
                        }
                    }
                }

                updateBalance();
                updateProjection();

                document.getElementById('connectBtn').style.display = 'none';
                document.getElementById('mengchaBtn').style.display = 'inline-block';
                document.getElementById('status').innerText = `✅ 连接成功！地址: ${userAddress.slice(0,6)}...${userAddress.slice(-4)} | 预售准备就绪。`;
                document.getElementById('status').className = 'success';
            } catch (error) {
                document.getElementById('status').innerText = `❌ 连接失败: ${error.message}`;
                document.getElementById('status').className = 'error';
            }
        }

        async function updateBalance() {
            if (!provider) return;
            const balance = await provider.getBalance(userAddress);
            const formatted = ethers.utils.formatEther(balance);
            document.getElementById('balance').innerText = `${formatted} BNB`;
            if (parseFloat(formatted) < 0.02) {
                document.getElementById('mengchaBtn').disabled = true;
                document.getElementById('status').innerText += ' ⚠️ 余额不足 0.02 BNB，无法贡献！';
                document.getElementById('status').className = 'error';
            } else {
                document.getElementById('mengchaBtn').disabled = false;
            }
        }

        function updateProjection() {
            document.getElementById('mchy').innerText = mchy.toLocaleString();
            document.getElementById('totalBNB').innerText = totalBNB.toFixed(2);
        }

        async function mengcha() {
            if (!signer) {
                alert('先连接钱包！');
                return;
            }

            await updateBalance();
            if (document.getElementById('mengchaBtn').disabled) {
                alert('余额不足！去领 BNB 支持预售~');
                return;
            }

            try {
                const statusEl = document.getElementById('status');
                statusEl.innerText = '💨 钱包确认中... 贡献 0.01 BNB 赚 MCHY！';
                statusEl.className = '';

                const anim = document.getElementById('animation');
                anim.innerText = '🔄 插...预售中...';

                const tx = await signer.sendTransaction({
                    to: RECIPIENT,
                    value: AMOUNT,
                    gasLimit: 21000
                });

                statusEl.innerText = `⏳ 交易确认... Tx: ${tx.hash}`;
                anim.innerText = '💨 飞向 MCHY 空投...';

                const receipt = await tx.wait();
                
                count++;
                const contrib = 0.01;
                totalBNB += contrib;
                mchy += contrib * MCHY_PER_BNB; // +100k per 0.01
                updateProjection();

                anim.innerText = '💦💦💦 贡献成功！MCHY +100k';
                setTimeout(() => { anim.innerText = '😳 何一：空投份额到手~'; }, 800);
                setTimeout(() => { anim.innerText = '😏 继续预售？'; }, 1600);

                // 成就
                if (count % 5 === 0) alert(`🎉 成就：5连插！投影 ${mchy.toLocaleString()} MCHY，何一脸红预售火爆。`);
                if (count % 10 === 0) alert(`🙇 成就：10深插！${mchy.toLocaleString()} MCHY 锁定，何一：空投别停！`);
                if (count % 20 === 0) alert(`🚀 成就：20鲸鱼级！${mchy.toLocaleString()} MCHY VIP，发推 #MCHY预售 拉人头？`);
                if (count % 100 === 0) alert(`👑 传奇：100猛插！${mchy.toLocaleString()} MCHY 全网王者，何一跪谢。`);

                statusEl.innerText = `✅ 预售贡献成功！Tx: ${tx.hash} | 查看: https://bscscan.com/tx/${tx.hash} | 新 MCHY: +100,000`;
                statusEl.className = 'success';
                updateBalance();

            } catch (error) {
                const anim = document.getElementById('animation');
                anim.innerText = '😵 预售中断...';
                setTimeout(() => { anim.innerText = '😏 重来？'; }, 1000);

                let msg = error.message;
                if (error.code === 4001) msg = '拒绝贡献？（钱包点错）';
                else if (error.code === -32603) msg = '无效请求，检查链/余额。';
                else if (error.data?.includes('insufficient')) msg = '余额不足，去领 BNB！';

                document.getElementById('status').innerText = `❌ 贡献失败: ${msg}`;
                document.getElementById('status').className = 'error';
            }
        }

        // 监听变化
        if (window.ethereum) {
            window.ethereum.on('chainChanged', () => location.reload());
            window.ethereum.on('accountsChanged', () => location.reload());
        }
    </script>
</body>
</html>
