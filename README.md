# 20151016

   OPpenTSDB 설치 중 에러 발생

    # 필요시 yum install git
    git clone git://github.com/OpenTSDB/opentsdb.git

    cd opentsdb
    yum install autoconf
    yum install automake
    [./build.sh  <- It takes about 10 minutes to complete.
    env COMPRESSION=NONE HBASE_HOME=/usr/local/data/hbase-1.1.2 ./src/create_table.sh]
    - 이 부분에서 에러 발생
    - 해결: 
    tsdtmp=${TMPDIR-'/usr/local/data'}/tsd
    mkdir -p "$tsdtmp"
