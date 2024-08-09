const PastebinAPI = require('pastebin-js'),
      pastebin = new PastebinAPI('EMWTMkQAVfJa9kM-MRUrxd5Oku1U7pgL');
const { makeid } = require('./id');
const QRCode = require('qrcode');
const express = require('express');
const path = require('path');
const fs = require('fs');
const pino = require("pino");
const {
    default: Venocyber_Tech,
    useMultiFileAuthState,
    Browsers,
    delay,
} = require("@whiskeysockets/baileys");

let router = express.Router();

function removeFile(FilePath) {
    if (!fs.existsSync(FilePath)) return false;
    fs.rmSync(FilePath, { recursive: true, force: true });
}

router.get('/', async (req, res) => {
    const id = makeid();
    async function VENOCYBER_MD_QR_CODE() {
        const { state, saveCreds } = await useMultiFileAuthState('./temp/' + id);
        try {
            let Qr_Code_By_Venocyber_Tech = Venocyber_Tech({
                auth: state,
                printQRInTerminal: false,
                logger: pino({ level: "silent" }),
                browser: Browsers.macOS("Desktop"),
            });

            Qr_Code_By_Venocyber_Tech.ev.on('creds.update', saveCreds);
            Qr_Code_By_Venocyber_Tech.ev.on("connection.update", async (s) => {
                const { connection, lastDisconnect, qr } = s;

                if (qr) {
                    try {
                        await res.end(await QRCode.toBuffer(qr));
                    } catch (error) {
                        console.error("Error generating QR code:", error);
                        res.status(500).json({ code: "Error generating QR code" });
                    }
                }

                if (connection === "open") {
                    await delay(5000);
                    try {
                        let data = fs.readFileSync(__dirname + `/temp/${id}/creds.json`);
                        let b64data = Buffer.from(data).toString('base64');
                        let session = await Qr_Code_By_Venocyber_Tech.sendMessage(Qr_Code_By_Venocyber_Tech.user.id, { text: '' + b64data });

                        let VENOCYBER_MD_TEXT = `*_Pair Code Connecte_*\n*_Made With RCD TEAM_*\n______________________________________\n╔══════════════════════❯\n║ *⛬ WOW YOU CHOOSEN RCD-MD ⛬*\n╚══════════════════════❯\n╔════════════════════❯\n║  ❮••• 𝗩𝗶𝘀𝗶𝘁 𝗙𝗼𝗿 𝗛𝗲𝗹𝗽 •••❯\n║➢  *Ytube:* ➖ *_https://rb.gy/1hcpmg_*\n║➢  *Repo:* ➖ *_https://rb.gy/fj7dc2_*\n║➢  *WaGroup:* ➖ *_https://rb.gy/ldoz3f_*\n║➢  *WaChannel:* ➖ *_https://rb.gy/91sc7k_*\n╚════════════════════❯\n\n> *RCD TEAM _____________________________*`;

                        await Qr_Code_By_Venocyber_Tech.sendMessage(Qr_Code_By_Venocyber_Tech.user.id, { text: VENOCYBER_MD_TEXT }, { quoted: session });
                        await delay(100);
                        await Qr_Code_By_Venocyber_Tech.ws.close();
                    } catch (error) {
                        console.error("Error during connection update:", error);
                        res.status(500).json({ code: "Error during connection update" });
                    } finally {
                        await removeFile("temp/" + id);
                    }
                    return;
                } else if (connection === "close" && lastDisconnect && lastDisconnect.error && lastDisconnect.error.output.statusCode != 401) {
                    await delay(10000);
                    VENOCYBER_MD_QR_CODE();
                }
            });
        } catch (err) {
            console.error("Error in VENOCYBER_MD_QR_CODE:", err);
            if (!res.headersSent) {
                res.status(500).json({ code: "Service is Currently Unavailable" });
            }
            await removeFile("temp/" + id);
        }
    }
    await VENOCYBER_MD_QR_CODE();
});

module.exports = router;
