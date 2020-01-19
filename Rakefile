desc "Construi o dicionário"
task :build do
  system %q(dictfmt --utf8 --allchars -s "Dicionário de Educação Brasileiro" -j edubr < dicionario.jargon)
end

desc 'Instala o dicionário.'
task :install do
  system %q(sudo cp edubr.dict edubr.index /usr/share/dictd/)
  system %q(sudo /usr/sbin/dictdconfig --write)
  system %q(sudo /etc/init.d/dictd restart)
end
