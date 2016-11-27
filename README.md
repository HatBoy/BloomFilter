# BloomFilter
Python+Redis实现的BloomFilter

利用Redis的setbit和getbit功能实现的BloomFilter，只需要输入预估要存储的数据量和错误率可自动计算需要的位数和最佳的hash次数，
根据需要的内存自动分块，每块内存512M，最多可使用256个内存块，去重的值第一个字符必须是ascii码，hash函数使用通用的murmurhash3算法，
如果没用输入redis连接，使用BitVector模块在内存中进行去重，此时只会使用一个512M的内存块进行去重，代码运行完后内存释放。具体使用方法见代码

#安装
###pip3 install murmurhash3
###pip3 install BitVector