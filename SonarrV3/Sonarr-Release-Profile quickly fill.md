Basically this is a guide on how to quickly fill SonarrV3 using TRASH- regex profile.

I'm posting TRASH- release profile Regex directly from his github.
You can check it out here (https://github.com/TRaSH-/Tutorials-FAQ/blob/master/SonarrV3/Sonarr-Release-Profile-RegEx.md).
```markdown
# Sonarr Release Profile RegEx
# This list is made by collecting information from Sonarr Discord Channel,
# and personal testing and a few others that helped.
# So I want to thnx everyone who helped to make this list possible,
# For privacy reasons I decided not to add the names/nick of the persons.
# If you want to be mentioned please message me on discord,
# including a link for proof to what part you want to be credited.


# Must Not Contain
/(x|h)\.?265/i, hevc

# Preferred
 [100]   /(amzn|amazon).?web.?dl/i
 [100]   /(atvp).?web.?dl/i
  [90]   /(dsnp|dsny|disney).?web.?dl/i
  [90]   /(nf|netflix).?web.?dl/i
  [85]   /(DCU).?web.?dl/i
  [85]   /(HMAX).?web.?dl/i
  [80]   /(-deflate|-inflate)/i
  [75]   /(hulu|.?hbo\.?)/i
  [75]   /(red).?web.?dl/i
  [75]   /(QIBI).?web.?dl/i
  [75]   /(iT).?web.?dl/i

  [50]   /(-AJP69|-BTN|-CasStudio|-CtrlHD|-KiNGS)/i
  [50]   /(-monkee|-MZABI|-NTb|-NTG|-QOQ|-RTN)/i
  [50]   /(-TOMMY|-ViSUM|-T6D)/i
  [25]   /(-BTW|-Chotab|-CiT|-DEEP|-iJP|-iT00NZ)/i
  [25]   /(-LAZY|-NYH|-SA89|-SIGMA|-TEPES|-TVSmash)/i
  [25]   /(-SDCC|-iKA|-iJP|-Cinefeel|-SPiRiT|-FC)/i
  [25]   /(-JETIX|-Coo7|-WELP|-KiMCHI|-BLUTONiUM)/i
  [25]   /(-orbitron|-ETHiCS|-RTFM)/i
  [12]   /(repack3)/i
  [11]   /(repack2)/i
  [10]   /(repack|proper)/i

  [-50]  /(-AMCON|-AMRAP|-BAMBOOZLE|-EDHD|-ION10)/i
  [-50]  /(-MEMENTO|-METCON|-POKE|-STARZ|-STRiFE)/i
  [-50]  /(-TRUMP|-WEBTiFUL|-JOMT|-APRiCiTY|-HILLARY)/i
  [-50]  /(-SQUEAK|-KOMPOST|-WNN|-LiGATE|-BTX|-ALiGN)/i
  [-50]  /(-BLACKHAT)/i
 [-100]  /(TBS|-BRiNK|-CHX|-XLF|-worldmkv|-GHOSTS)/i

# Optional (use these only if you dislike renamed and retagged releases)
  [-25]  /(\[rartv\]|\[eztv\]|\[TGx\])/i
  [-25]  /(-4P|-4Planet|-AsRequested|-BUYMORE)/i
  [-25]  /(-Chamele0n|-GEROV|-iNC0GNiTO|-NZBGeek)/i
  [-25]  /(-Obfuscated|-postbot|-Rakuv|-Scrambled)/i
  [-25]  /(-WhiteRev|-xpost)/i
# Optional (matches releases that ends with EN)
  [-25]  /\s?\ben\b$/i
# Optional Matches any release that contains '1-' as prefix for Release Groups
  [-25]  /(1-.+)$/i
# Optional Matches Season Packs (use this if you prefer Season packs)
  [15]   /\bS\d+\b(?!E\d+\b)/i
```



  Basically these are the steps you have to do:
  1. Go to sonarr release profile page
  2. Press the + to create a release profile page
  3. Press F12 to enter the console
  4. Run this command
  ```markdown
  // https://github.com/facebook/react/issues/11488#issuecomment-347775628
const changeValue = (input, value) => {
  let lastValue = input.value;
  input.value = value;
  const event = new Event('input', { bubbles: true });
  // React16 hack
  const tracker = input._valueTracker;
  tracker && tracker.setValue(lastValue);
  input.dispatchEvent(event);
}

let populate = (score, groups) => {
  const arr = groups.split(',');
  for (let i = 0; i < arr.length; i++) {
    changeValue($('.KeyValueListInputItem\\/keyInput\\/3YYEs')[i], arr[i]);
    changeValue($('.KeyValueListInputItem\\/valueInput\\/3zlQA')[i], score);
  }
}
```

5. follow with 
```markdown
populate(100,'/(amzn|amazon).?web.?dl/i,/(atvp).?web.?dl/i,/(dsnp|dsny|disney).?web.?dl/i,/(nf|netflix).?web.?dl/i,/(DCU).?web.?dl/i,/(HMAX).?web.?dl/i,/(-deflate|-inflate)/i,/(hulu|.?hbo\.?)/i,/(red).?web.?dl/i,/(QIBI).?web.?dl/i,/(iT).?web.?dl/i,/(-AJP69|-BTN|-CasStudio|-CtrlHD|-KiNGS)/i,/(-monkee|-MZABI|-NTb|-NTG|-QOQ|-RTN)/i,/(-TOMMY|-ViSUM|-T6D)/i,/(-BTW|-Chotab|-CiT|-DEEP|-iJP|-iT00NZ)/i,/(-LAZY|-NYH|-SA89|-SIGMA|-TEPES|-TVSmash)/i,/(-SDCC|-iKA|-iJP|-Cinefeel|-SPiRiT|-FC)/i,/(-JETIX|-Coo7|-WELP|-KiMCHI|-BLUTONiUM)/i,/(-orbitron|-ETHiCS|-RTFM)/i,/(repack3)/i,/(repack2)/i,/(repack|proper)/i,/(-AMCON|-AMRAP|-BAMBOOZLE|-EDHD|-ION10)/i,/(-MEMENTO|-METCON|-POKE|-STARZ|-STRiFE)/i,/(-TRUMP|-WEBTiFUL|-JOMT|-APRiCiTY|-HILLARY)/i,/(-SQUEAK|-KOMPOST|-WNN|-LiGATE|-BTX|-ALiGN)/i,/(-BLACKHAT)/i,0,/(TBS|-BRiNK|-CHX|-XLF|-worldmkv|-GHOSTS)/i,/(\[rartv\]|\[eztv\]|\[TGx\])/i,/(-4P|-4Planet|-AsRequested|-BUYMORE)/i,/(-Chamele0n|-GEROV|-iNC0GNiTO|-NZBGeek)/i,/(-Obfuscated|-postbot|-Rakuv|-Scrambled)/i,/(-WhiteRev|-xpost)/i')
```

6. Now you have a quick list and all you have to do is change the numbers based on trash- regex list :)


