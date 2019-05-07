file "Regular/OTC/SourceHanSans-Regular.otf" do |t|
  cd "Regular/OTC" do
    sh "makeotf -f cidfont.ps.OTC.J -omitMacNames -ff features.OTC.J -fi cidfontinfo.OTC.J -mf ../../FontMenuNameDB -r -nS -cs 1 -ch ../../UniSourceHanSansJP-UTF32-H -ci ../../SourceHanSans_JP_sequences.txt"
    sh "tx -cff +S -no_futile cidfont.ps.OTC.J CFF.OTC.J"
    sh "sfntedit -a CFF=CFF.OTC.J SourceHanSans-Regular.otf"
  end
end

file "Regular/OTC/SourceHanSansHW-Regular.otf" do |t|
  sh "tx -cff -fdx 8 Regular/OTC/cidfont.ps.OTC.HW.J > stripped.pfb"
  sh "mergefonts -cid Regular/OTC/cidfontinfo.OTC.HW.J merged.pfb stripped.pfb cmu.map CMU/cmuntt.pfb"
  # sh "tx -pdf merged.pfb > test_merged.pdf"
  cd "Regular/OTC" do
    # sh "makeotf -f cidfont.ps.OTC.HW.J -omitMacNames -ff features.OTC.HW.J -fi cidfontinfo.OTC.HW.J -mf ../../FontMenuNameDB.HW -r -nS -cs 1 -ch ../../UniSourceHanSansHWJP-UTF32-H -ci ../../SourceHanSans_JP_sequences.txt"
    sh "makeotf -f ../../merged.pfb -omitMacNames -ff features.OTC.J -fi cidfontinfo.OTC.J -mf ../../FontMenuNameDB -r -nS -cs 1 -ch ../../UniSourceHanSansJP-UTF32-H -ci ../../SourceHanSans_JP_sequences.txt"
    sh "tx -cff +S -no_futile ../../merged.pfb CFF.OTC.HW.J"
    sh "sfntedit -a CFF=CFF.OTC.HW.J SourceHanSansHW-Regular.otf"
  end
end

file "jodoji.otf" do |t|
  cd "Regular/OTC" do
  sh "makeotf -f cidfont.ps.OTC.HW.J -omitMacNames -ff features.OTC.HW.J -fi cidfontinfo.OTC.HW.J -mf ../../FontMenuNameDB.HW -r -nS -cs 1 -ch ../../UniSourceHanSansHWJP-UTF32-H -ci ../../SourceHanSans_JP_sequences.txt"
  sh "tx -cff +S -no_futile cidfont.ps.OTC.HW.J CFF.OTC.HW.J"
  sh "sfntedit -a CFF=CFF.OTC.HW.J SourceHanSansHW-Regular.otf"
  end
end

task :default => "Regular/OTC/SourceHanSansHW-Regular.otf"
