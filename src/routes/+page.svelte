<div id="canvas"></div>
I cant get this QR CODE to work 
<script>
   
    import QRCodeStyling from "qr-code-styling";

    import { onMount } from 'svelte';
    
    onMount(async () => {

        let id = document.getElementById("canvas");
        
        const qrCode = new QRCodeStyling({
            width: 300,
            height: 300,
            image:
            "https://upload.wikimedia.org/wikipedia/commons/5/51/Facebook_f_logo_%282019%29.svg",
                dotsOptions: {
                color: "#4267b2",
                type: "rounded"
            },
            imageOptions: {
                crossOrigin: "anonymous",
                margin: 20
            }
        });
        qrCode.append(id);
        qrCode.download({ name: "qr", extension: "svg" });
    });
</script>


