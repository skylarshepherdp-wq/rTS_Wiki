---
title: Blackscreen issue that occurs after enabling Secureboot
sidebar:
    hidden: false
pagefind: true
tableOfContents: true
---
When enabling Secure Boot there is a chance that the motherboard will stop recognizing the current GPU and just give a black screen. We have no idea why it happens. The board will sometimes show a debug LED for VGA, sometimes not.

The only solution we have found is removing the GPU and using the iGPU if the system has integrated graphics, or replacing the GPU. Once replaced, you can disable Secure Boot, put the old GPU back and try enabling it again. We've seen one case where the user had it happen three times in a row, but it worked on the fourth try.

Resetting the CMOS hasn't had any effect. Uncertain about Flashback (Flash BIOS button), worth a shot if you don't have an iGPU or a second GPU at hand.

One other potential cause is an outdated motherboard BIOS/UEFI firmware that lacks proper compatibility related to Secure Boot. Updating your motherboard's BIOS to the latest version provided by the manufacturer has resolved this issue before. Determine the exact manufacturer and model number of your motherboard. Visit your motherboard manufacturer's official support website. Search for your exact motherboard model, navigate to the Support or Downloads section, then download the latest BIOS/UEFI firmware available for your motherboard.Each manufacturer provides its own BIOS update procedure and utility (such as ASUS EZ Flash, MSI M-Flash, Gigabyte Q-Flash, or ASRock Instant Flash). Carefully follow the official instructions provided by the manufacturer.After the BIOS update completes: Enter the BIOS/UEFI setup, restore any custom settings that may have been reset, re-enable Secure Boot if it is disabled, save the changes and restart the computer. After updating to the latest BIOS revision systems affected by firmware-related Secure Boot issues may boot normally with Secure Boot enabled, eliminating the black screen experienced on startup.
