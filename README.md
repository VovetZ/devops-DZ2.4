# devops-DZ2.4

## 1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.
*git show aefea --pretty='%H %an'  -s*
  
aefead2207ef7e2aa5dc81a34aedf0cad4c32545 Alisdair McDiarmid

##  2. Какому тегу соответствует коммит 85024d3?
*git describe --tags 85024d3*
  
v0.12.23

  ##  3. Сколько родителей у коммита b8d720? Напишите их хеши.
 Два родителя.
  
 *git show  --pretty='%P%n' b8d720*
  
56cd7859e05c36c06b56d013b55a252d0bb7e158 
9ea88f22fc6269854151c571162c5bcf958bee2b


  ##  4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.

*git log v0.12.23...v0.12.24 --pretty='%H %s' --reverse*
  
225466bc3e5f35baa5d07197bbc079345b77525e Cleanup after v0.12.23 release

dd01a35078f040ca984cdd349f18d0b67e486c35 Update CHANGELOG.md

4b6d06cc5dcb78af637bbb19c198faff37a066ed Update CHANGELOG.md

d5f9411f5108260320064349b757f55c09bc4b80 command: Fix bug when using terraform login on Windows

06275647e2b53d97d4f0a19a0fec11f6d69820b5 Update CHANGELOG.md

5c619ca1baf2e21a155fcdb4c264cc9e24a2a353 website: Remove links to the getting started guide's old location

6ae64e247b332925b872447e9ce869657281c2bf registry: Fix panic when server is unreachable

3f235065b9347a758efadc92295b540ee0a5e26e Update CHANGELOG.md

b14b74c4939dcab573326f4e3ee2a62e23e12f89 [Website] vmc provider links

33ff1c03bb960b332be3af2e333462dde88b279e v0.12.24

## 5. Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит так func providerSource(...) (вместо троеточего перечислены аргументы).##
*git log -SproviderSource  --pretty=format:'%h %an -- %s -- %ad' --reverse -n 1*

5e06e39fc findkim -- Use registry alias to fetch providers -- Wed Nov 28 10:26:16 2018 -0600

## 6. Найдите все коммиты в которых была изменена функция globalPluginDirs.##

*git log -SglobalPluginDirs  --pretty=format:'%h %an -- %s -- %ad'*

125eb51dc Alisdair McDiarmid -- Remove accidentally-committed binary -- Thu May 5 10:12:00 2022 -0400

22c121df8 Anna Winkler -- Bump compatibility version to 1.3.0 for terraform core release (#30988) -- Tue May 3 12:28:41 2022 -0600

35a058fb3 Martin Atkins -- main: configure credentials from the CLI config file -- Thu Oct 19 17:40:20 2017 -0700

c0b176109 James Bardin -- prevent log output during init -- Mon Jun 12 15:04:40 2017 -0400

8364383c3 Martin Atkins -- Push plugin discovery down into command package -- Thu Apr 13 18:05:58 2017 -0700

##  7. Кто автор функции synchronizedWriters? ##

*git log -SsynchronizedWriters  --pretty=format:'%h %an -- %s -- %ad'*

bdfea50cc James Bardin -- remove unused -- Mon Nov 30 18:02:04 2020 -0500

fd4f7eb0b James Bardin -- remove prefixed io -- Wed Oct 21 13:06:23 2020 -0400

**5ac311e2a Martin Atkins -- main: synchronize writes to VT100-faker on Windows -- Wed May 3 16:25:41 2017 -0700**
