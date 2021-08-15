<script>
    import { ethers } from 'https://cdn.ethers.io/lib/ethers-5.1.esm.min.js';
    import makeBlockie from 'https://cdn.skypack.dev/ethereum-blockies-base64';

    const wallet = ethers.Wallet.createRandom();
</script>

<main class="card my-6 bordered shadow-sm bg-base-200 p-6 text-accent flex items-center">
    <div class="">
        <img
            src={makeBlockie(wallet.address)}
            alt="blockie"
            class="mask mask-circle border-1 border-white"
            width="64"
            height="64"
        />
    </div>
    <div class="">
        <div>{wallet.mnemonic.phrase}</div>
        <div>{wallet.mnemonic.path}</div>
        <div>{wallet.privateKey}</div>
        <div>{wallet.address}</div>
    </div>
</main>
